# Sistem Peminjaman Ruangan
# Kelompok
| Nama                      | NIM           | Akun Github   |
| ------------              | --------------| --------------|
| Dewa Ayu Sarika Citra     | 2501010134    | nimadeerap-ui |
| Ni Made Era Purnama Dewi  | 2501010007    | dwyu0-ui      |

# 📌 Rumusan Masalah
1. Bagaimana penerapan struktur data queue dalam mengelola sistem peminjaman ruangan secara teratur?
2. Bagaimana implementasi queue menggunakan array dalam mengatur antrian peminjaman ruangan?
3. Bagaimana sistem antrian yang dibuat dapat meningkatkan efisiensi dan keadilan dalam proses peminjaman ruangan?

# 📌 Solusi
- Untuk menjawab permasalahan tersebut, dirancang sebuah sistem peminjaman ruangan menggunakan struktur data queue dengan prinsip FIFO (First In First Out). Sistem ini memastikan bahwa setiap permintaan peminjaman diproses berdasarkan urutan waktu pengajuan.
- Implementasi dilakukan menggunakan array dengan operasi utama enqueue, dequeue, peek, dan display. Dengan sistem ini, proses peminjaman menjadi lebih terstruktur, efisien, dan adil.

# 📌 Landasan Teori
## Sumber ilmiah
- Algoritma dan Struktur Data – Queue
- Perancangan dan Implementasi Website Sistem Antrian Bank Berbasis Queue untuk Efisiensi Pelayanan Nasabah.
- Analisis Teori Antrian Multi-Channel dengan Distribusi Eksponens
- Ramadhan, R., dkk. (2026). Implementasi Algoritma Priority Scheduling – FIFO pada Sistem Informasi Peminjaman Ruangan. JATI.
- Widyawati, dkk. (2025). Rancang Bangun Sistem Peminjaman Barang dan Ruangan Berbasis Website. IFTECH.
- Cormen, T. H., dkk. (2009). Introduction to Algorithms. MIT Press.
- Laudon, K. C., & Laudon, J. P. (2018). Management Information Systems. Pearson.
## Pengertian struktur data
- Dalam istilah ilmu komputer, struktur data adalah cara penyimpanan , pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien. Dalam teknik pemrograman, struktur data berarti tata letak data yang berisi kolom-kolom data,baik itu kolom yang tampak oleh pengguna (user) ataupunkolom yang hanya digunakan untuk keperluan pemrograman yang tidak tampak oleh pengguna. Setiap baris dari kumpulan kolom-kolom tersebut dinamakan catatan (record).
- Struktur Data adalah cara 
mengumpulkan dan mengatur data sedemikian rupa sehingga kita dapat melakukan operasi pada sebuah data dengan cara yang efektif. Struktur Data adalah tentang merender elemen data dalam beberapa hubungan, untuk organisasi dan penyimpanan yang lebih baik.
- Struktur data merujuk pada cara data diatur dan disimpan di dalam komputer atau penyimpanan lainnya agar dapat diakses dan dimanipulasi dengan efisien. Dalam pemrograman, pemilihan jenis struktur data memiliki dampak yang signifikan pada kinerja program, kompleksitas kode, dan penggunaan sumber daya komputer.

## Konsep queue 
- Dalam ilmu komputer dikenal konsep struktur data queue yang menerapkan prinsip 
First In First Out (FIFO), yaitu data yang pertama masuk akan diproses lebih dahulu. Penerapan teori antrian atau queueing theory juga memberikan dasar ilmiah untuk memodelkan laju kedatangan, laju pelayanan, dan estimasi waktu tunggu, sehingga mampu meningkatkan efisiensi pelayanan publik. 
- Di dalam setiap layanan, antrian berjalan dengan prinsip FIFO (First In First Out), di mana nasabah yang pertama masuk akan dilayani lebih dahulu.
- Kejadian antrian (queues) terjadi karena permintaan pelayanan lebih besar daripada fasilitas pelayan yang ada dalam sistem antrian. Permintaan pelayanan akan meningkat terus menerus sedangkan ketersediaan fasilitas pelayanan terbatas. Antrian menimbulkan berbagai kerugian (loss), opportunity loss dan wasting time. Antrian yang terlalu panjang memungkinkan terjadinya jockeying (berpindah dari antrian satu ke antrian lainnya), balking (penolakan) dan reneging (pembatalan) sehingga akan merugikan pihak yang membutuhkan layanan. Untuk mengurangi kerugian dalam antrian, perlu dilakukan peningkatan efisiensi sistem antrian
## Konsep FIFO 
- Elemen yang pertama kali masuk ke dalam sistem akan diproses paling awal mengikuti alur antrean yang ada..
- Menjamin aspek keadilan antrian (fairness), namun memiliki kelemahan dalam mengakomodasi situasi mendesak (urgency). Priority Scheduling digunakan untuk menangani urgensi, dan FIFO digunakan untuk menjaga keadilan saat urgensi setara.
- The system enforces a First In, First Out (FIFO) mechanism, promoting fairness and orderliness in resource distribution.
- metode FIFO (First In First Out) digunakan untuk memastikan urutan pengajuan diproses dengan adil
## Implementasi menggunakan array 
## 1️⃣ Inisialisasi
```python
queue = []
max_size = 5
```
## 2️⃣ ENQUEUE (MENAMBAHKAN ANTRIAN)
```python
def enqueue(data):
  if len(queue)>=max_size:
    print("ANTRIAN PENUH!")
  else:
    queue.append(data)
    print("Ditambahkan keantrian:",data)
```
## 3️⃣ DEQUEUE (PROSES ANTRIAN)
```python
def dequeue():
  if not queue:
    print("Antrian kosong")
  else:
    print("Sudah di proses:",queue.pop(0))
```
## 4️⃣ DISPLAY (MENAMPILKAN SEMUA DATA)
```python
def display():
  if not queue:
    print("Antrian kosong")
  else:
    print("\n Daftar antrian peminjaman:")
    for i, data in enumerate(queue):
      print(i+1,".",data)
```
## 5️⃣ PEEK (MELIHAT ANTRIAN TERDEPAN)
```python
def peek():
  if queue:
    print("Antrian terdepan:",queue[0])
  else:
    print("Antrian kosong")
```
## 6️⃣PENGAPLIKASIAN
```python
enqueue ("Era minjem ruangan 515, jam 10.00-12.20 untuk rapat organisasi")
enqueue ("Wilsa minjem ruangan 331, jam 07.30-10.00 untuk kelas pengganti")
enqueue ("ceri minjem ruangan lab k, jam 10.00-12.20 untuk membuat web")

display()
peek()
dequeue()
display()
```
# 📌 Desain Sistem dan Implementasi
Jelaskan desain sistem menggunakan salah satu berikut:
- Flowchart
adalah diagram yang digunakan untuk menggambarkan alur proses dalam suatu sistem secara sistematis menggunakan simbol tertentu. Selain itu flowchart juga membantu dalam memahami logika program sebelum diimplementasikan ke dalam kode. Dalam sistem peminjaman ruangan berbasis queue ini, flowchart digunakan untuk menggambarkan alur mulai dari input data peminjam, proses penambahan antrian (enqueue), pemrosesan antrian (dequeue), hingga menampilkan data (display) dan melihat antrian terdepan (peek).

Adapun simbol-simbol yang digunakan dalam flowchart sistem peminjaman ruangan, yaitu:

- Terminator (oval) → menunjukkan awal (Mulai) dan akhir (Selesai) proses
- Process (persegi panjang) → digunakan untuk proses display, peek, dequeue, dan enqueue
- Decision (belah ketupat) → digunakan untuk kondisi seperti apakah antrian kosong atau apakah antrian penuh
- Input/Output (jajar genjang) → untuk menampilkan hasil seperti “Antrian kosong” atau daftar antrian
- Flowline (panah) → menunjukkan arah alur proses
  
<img width="276" height="382" alt="WhatsApp Image 2026-04-24 at 10 25 13" src="https://github.com/user-attachments/assets/c332d760-2e38-40b3-9948-e5f6de08e8e3" />



# 📌 Kesimpulan
- Berdasarkan hasil implementasi, struktur data queue berhasil diterapkan dalam sistem peminjaman ruangan. Rumusan masalah yang diajukan telah terjawab melalui sistem yang dibuat.
- Sistem berjalan sesuai dengan konsep FIFO, di mana data yang pertama masuk akan diproses terlebih dahulu. Hal ini membuktikan bahwa queue sangat efektif dalam mengelola antrian.
- Penggunaan queue memberikan manfaat berupa keteraturan, keadilan, dan efisiensi dalam proses peminjaman ruangan.

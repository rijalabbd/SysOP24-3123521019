
---

# Memahami Perbedaan Serial, Parallel, Concurrent, dan Concurrent Parallel

![Screenshot 2024-05-19 162648](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/50ca59b8-5f35-46b6-aca4-fd258913e13f)

## Serial
- **Definisi:** Eksekusi tugas dilakukan secara berurutan, satu demi satu.
- **Tampilan:** Seperti antrian, di mana proses dikerjakan satu per satu.
- **Contoh:** Menonton film, mengerjakan soal matematika.

## Parallel
- **Definisi:** Eksekusi tugas dilakukan secara bersamaan, memanfaatkan beberapa sumber daya (seperti CPU) secara simultan.
- **Tampilan:** Seperti balapan, di mana beberapa pelari berlari secara bersamaan.
- **Contoh:** Mengunduh beberapa file secara bersamaan, menonton video sambil browsing internet.

## Concurrent
- **Definisi:** Eksekusi tugas dilakukan secara bergantian, seolah-olah bersamaan, tetapi tidak benar-benar simultan.
- **Tampilan:** Seperti multitasking, di mana satu orang mengerjakan beberapa tugas secara bergantian.
- **Contoh:** Mendengarkan musik sambil mengerjakan tugas, menjawab panggilan telepon sambil mengetik pesan.

## Concurrent Parallel
- **Definisi:** Kombinasi dari **Concurrent** dan **Parallel**, di mana beberapa tugas dijalankan secara bersamaan (parallel) dan beberapa tugas lainnya dijalankan secara bergantian (concurrent).
- **Tampilan:** Seperti orkestra, di mana beberapa instrumen dimainkan secara bersamaan dan beberapa instrumen lainnya dimainkan secara bergantian untuk menciptakan harmoni.
- **Contoh:** Rendering video sambil menjalankan aplikasi lain, bermain game online sambil chatting dengan teman.

---

## Contoh Kasus

### Bounded-Buffer Problem
![Screenshot 2024-05-19 162857](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d873ae0b-f9e2-4548-a1f7-dbee647cfc1d)
- **Situasi:** Produsen memproduksi item dan memasukkannya ke dalam buffer. Konsumen mengambil item dari buffer. Buffer memiliki kapasitas terbatas.
- **Masalah:** Sinkronisasi antara produsen dan konsumen untuk menghindari buffer overflow (penuh) atau underflow (kosong).
- **Solusi:** Semaphore digunakan untuk mengontrol akses produsen dan konsumen ke buffer, memastikan ketersediaan buffer dan menghindari konflik.

### Readers and Writers Problem
- **Situasi:** Beberapa pembaca (readers) dapat mengakses data secara bersamaan, tetapi hanya satu penulis (writer) yang dapat mengakses data pada satu waktu.
- **Masalah:** Sinkronisasi antara pembaca dan penulis untuk menghindari pembacaan data yang tidak konsisten oleh pembaca saat penulis sedang menulis data.
- **Solusi:** Reader-writer locks atau semaphores digunakan untuk mengontrol akses pembaca dan penulis ke data, memastikan konsistensi data.

### Dining Philosophers Problem
- **Situasi:** Lima filsuf (philosophers) duduk di meja makan dengan lima garpu (forks). Setiap filsuf membutuhkan dua garpu untuk makan, tetapi hanya ada lima garpu.
- **Masalah:** Mencegah deadlock (kebuntuan) di mana semua filsuf tertahan karena masing-masing hanya memiliki satu garpu dan tidak dapat mengambil garpu kedua.
- **Solusi:** Algoritma seperti dining philosophers problem algorithms digunakan untuk mengatur akses filsuf ke garpu, memastikan semua filsuf dapat makan tanpa deadlock.

---

## Penjelasan Gambar

### Shared Resource antara Writers dan Readers
![Screenshot 2024-06-02 135133](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/ebe8d49e-cdd8-43e6-9819-bf50af34192e)

Gambar di atas menunjukkan diagram representasi masalah pembaca-penulis (reader-writer problem) dalam sistem operasi. Masalah ini menggambarkan situasi di mana beberapa proses (pembaca dan penulis) perlu mengakses sumber daya bersama (seperti file atau database) dengan cara yang saling eksklusif, menghindari konflik, dan memastikan ketepatan data.

#### Komponen Utama Diagram
- **Sumber Daya Bersama (Shared Resource):** Data yang diakses oleh pembaca dan penulis. Sumber daya ini dapat berupa file, database, atau struktur data lainnya.
- **Pembaca (Readers):** Proses yang mengakses sumber daya untuk membaca dan tidak mengubahnya. Pembaca dapat mengakses sumber daya secara bersamaan, asalkan tidak ada penulis yang aktif.
- **Penulis (Writers):** Proses yang mengakses sumber daya untuk mengubahnya. Penulis harus memiliki akses eksklusif ke sumber daya untuk memastikan data tidak terkontaminasi oleh pembaca atau penulis lain.

#### Alur Operasi
Diagram menunjukkan urutan langkah yang diambil oleh pembaca dan penulis untuk mengakses sumber daya bersama:

**Pembaca (Readers)**
1. **EnterReader():** Pembaca memasuki area kritis untuk mengakses sumber daya.
2. **Read(...):** Pembaca membaca data dari sumber daya.
3. **LeaveReader():** Pembaca meninggalkan area kritis, memungkinkan pembaca atau penulis lain untuk mengakses sumber daya.

**Penulis (Writers)**
1. **EnterWriter():** Penulis memasuki area kritis untuk mengakses sumber daya.
2. **Write(...):** Penulis mengubah data dalam sumber daya.
3. **LeaveWriter():** Penulis meninggalkan area kritis, memungkinkan pembaca atau penulis lain untuk mengakses sumber daya.

#### Mekanisme Sinkronisasi
Untuk menjaga konsistensi data dan menghindari konflik, mekanisme sinkronisasi seperti semaphore, mutex, atau monitor digunakan. Mekanisme ini memastikan bahwa hanya satu penulis yang dapat mengakses sumber daya pada satu waktu, dan tidak ada penulis yang dapat mengakses sumber daya saat ada pembaca yang aktif.

### Dining Philosophers Problem
![Screenshot 2024-06-02 135532](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/769a06ef-ffbf-4503-a38c-5092f68d0044)

Dining Philosophers Problem adalah masalah klasik dalam ilmu komputer yang menggambarkan sinkronisasi dan deadlock dalam sistem konkuren. Diperkenalkan oleh Edsger Dijkstra pada tahun 1965, masalah ini menggambarkan situasi di mana lima filsuf duduk di meja bundar dengan satu piring spaghetti di depan masing-masing. Ada garpu di antara setiap dua filsuf, dan setiap filsuf membutuhkan dua garpu untuk makan.

#### Solusi: Waiter
Solusi sederhana ini melibatkan seorang waiter yang mengawasi penggunaan sumpit di meja makan. Ketika empat buah (dua pasang) sumpit sedang dipakai, orang berikutnya yang ingin memakai sumpit harus meminta izin kepada sang waiter, yang hanya dapat diberi ketika salah satu sumpit telah selesai terpakai.

**Contoh:**
Misalkan ke-lima orang tersebut dinamakan dari A sampai E secara berurutan.

Ketika A dan C sedang makan, 4 buah sumpit sedang terpakai. B tidak memiliki kedua sumpit, dan D serta E memiliki satu buah sumpit di antara mereka.

Apabila D ingin makan dan mengambil sumpit kelima, deadlock sangat mungkin terjadi. Maka waiter akan meminta D untuk menunggu, hingga salah satu sumpit selesai digunakan.

---


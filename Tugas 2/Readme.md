# tugas 2

## Daftar tugas
- [mind map](https://github.com/rijalabbd/SysOP24-3123521019/blob/main/Tugas%202/Readme.md#proses-booting)

 ## Proses Booting
 Booting:
-Adalah proses di mana sebuah komputer atau perangkat elektronik lainnya diaktifkan atau dinyalakan untuk memulai dan mempersiapkan diri untuk digunakan. Proses booting ini melibatkan beberapa tahapan, termasuk pengalihan daya ke perangkat keras, pengujian perangkat keras untuk memastikan semuanya berfungsi dengan baik (biasanya disebut POST - Power-On Self Test), dan memuat sistem operasi atau perangkat lunak lainnya ke dalam memori untuk menjalankan program-program yang diperlukan. Booting merupakan langkah awal yang penting sebelum sebuah komputer atau perangkat elektronik dapat digunakan secara normal.

Berikut adalah beberapa contoh situasi di mana proses booting terjadi:
- *Menyalakan Komputer*: Ketika Anda menyalakan komputer Anda, proses booting dimulai. Pada tahap awal ini, daya diarahkan ke perangkat keras, seperti motherboard, CPU, RAM, dan penyimpanan. Kemudian, POST (Power-On Self Test) dijalankan untuk memeriksa apakah perangkat keras berfungsi dengan baik.
-  *Memulai Sistem Operasi*: Setelah perangkat keras telah diperiksa dan diinisialisasi, sistem operasi yang terinstal (seperti Windows, macOS, atau Linux) dimuat ke dalam memori dari penyimpanan. Ini mengizinkan sistem operasi untuk mengambil kendali atas komputer dan memberikan antarmuka kepada pengguna untuk memulai penggunaan yang normal.
- *Restart Komputer*: Ketika Anda merestart komputer Anda, proses booting juga terjadi. Ini termasuk menghentikan dan memulai ulang sistem operasi dan memuat kembali semua perangkat lunak yang mungkin berjalan sebelumnya.

![WhatsApp Image 2024-03-01 at 18 46 22_1fedac15](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/91ddf031-6578-45e9-8436-6175b36cf989)

Kemudian diatas adalah diagram contoh dari proses booting

Penjelasan Dan Analisis Diagram: 
1. System powers up, Processor starts receiving reliable power

 Analisis:
- Sistem dinyalakan.
- Prosesor mulai menerima daya yang stabil.
- Prosesor menginisialisasi dan mengeksekusi bootloader awal.
- Prosesor mulai mencari perangkat penyimpanan yang valid.

2. System powers up, Processor starts receiving reliable power

Analisis
-Sistem dinyalakan:
  Tekan tombol power.
  Listrik mengalir ke motherboard dan prosesor.
-Prosesor aktif dan menjalankan BIOS:
  Memeriksa internal & memuat BIOS dari ROM/flash memory.
-Memuat initial bootloader:
  BIOS mencari & memuat bootloader dari perangkat penyimpanan.

3. Essential system peripherals OK?

Analisis:

- Sistem melakukan scan untuk memeriksa apakah semua perangkat periferal sistem penting berfungsi 
  dengan baik.
- Jika semua perangkat periferal berfungsi dengan baik, lanjutkan ke langkah berikutnya.
- Jika ada perangkat periferal yang tidak berfungsi dengan baik, sistem akan menampilkan pesan error dan 
   berhenti.

4. Scan storage devices for secondary bootloader

Analisis:

- Sistem melakukan scan pada semua perangkat penyimpanan untuk mencari bootloader sekunder.
- Jika bootloader sekunder ditemukan, lanjutkan ke langkah berikutnya.
- Jika bootloader sekunder tidak ditemukan, sistem akan menampilkan pesan error dan berhenti.

5. Error state

Analisis

- Kondisi: Error saat instalasi sistem operasi.
- Penyebab: Sistem operasi tidak valid.
                    Perangkat penyimpanan bermasalah.
                    Kesalahan konfigurasi.
- Tindakan: Menampilkan pesan error & penyebabnya.
                  Memberi opsi:
                      Memperbaiki error.
                      Membatalkan instalasi.

6.  Located valid storage device?

Analisis:

- Jika perangkat penyimpanan yang valid ditemukan, lanjutkan ke langkah berikutnya.
- Jika tidak ada perangkat penyimpanan yang valid ditemukan, sistem akan menampilkan pesan error dan 
  berhenti.

7. Scan for valid operating system

Analisis:
- Tahap: Setelah pemeriksaan perangkat periferal.
- Proses: Memeriksa semua perangkat penyimpanan untuk sistem operasi yang valid.
- Validasi: Sistem operasi memiliki file & terdaftar di tabel partisi.
- Hasil:Ditemukan: lanjut instalasi.
           Tidak ditemukan: error & berhenti.

8. Located valid OS?

Analisis:

- Sistem memeriksa apakah terdapat sistem operasi yang valid pada perangkat penyimpanan.
- Jika sistem operasi yang valid ditemukan, lanjutkan ke langkah berikutnya.
- Jika tidak ada sistem operasi yang valid ditemukan, sistem akan menampilkan pesan error dan berhenti.

9. Copy OS to RAM, execute OS

Analisis:

- Sistem menyalin file-file sistem operasi ke dalam RAM.
- Sistem mengeksekusi sistem operasi.
- Sistem operasi akan memulai proses booting dan menampilkan desktop.

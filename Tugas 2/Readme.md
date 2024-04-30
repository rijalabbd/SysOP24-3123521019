# tugas 2

## Daftar tugas
- [Proses booting](https://github.com/rijalabbd/SysOP24-3123521019/blob/main/Tugas%202/Readme.md#proses-booting)
- [Mendefinisikan spec laptop]()

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

##Spesifikasi Laptop Saya
![Screenshot 2024-02-29 141845](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/83dfa566-65cb-4302-b51c-f367c29ce878)


Cpu: Dari gambar di atas menunjukan tentang infromasi prosesor, seperti nama, kode nama,package, technology, spesifikasi dan kecepatan clock

- Prosesor: Menunjukan nama prosesor yang digunakan"Intel Core 17 12700H 12th Generation"
- Code Name: Menunjukan kode nama prosesor"Alder Lake"
- Package: Menunjukan jenis paket yang digunakan oleh prosesor: Socket 1744FCBGA"
- Technolgy: Menujukan proses manufaktur yang digunakan oleh prosesor"10 nm"
- Spesification: Menunjukan nama lengkap prosesor dan nama model
- Family: Menunjukan nama keluarga dari prosesor"6"
- Model: Menunjukan model prosesor"i7"
- Instructions: Menunjukkan daftar instruksi yang didukung oleh prosesor

- Core Speed: Menunjukkan kecepatan clock saat ini dari inti prosesor"3192.19MHz"
- Multiplier: Menunjukkan pengganda yang digunakan untuk menentukan kecepatan clock inti.
- Bus Speed: Menunjukkan kecepatan bus yang menghubungkan prosesor ke memori dan perangkat lain.
Bagian Cache: 

- L1 Data: Menunjukkan ukuran cache L1 data"6 x 48 KB + 8 x 32 KB"
- L1 Instruction: Menunjukkan ukuran cache L1 Instructions"6 x 32 KB + 8 X 32 KB"
- Level 2: Menunjukkan ukuran cache L2,"6 x 1.25MB + 2x 2 MB".
- Level 3: Menunjukkan ukuran cache L3,"24 MByets".

![Screenshot 2024-02-29 142807](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/9767d8ec-6091-4734-bf7b-13ee69440dd0)
Informasi Motherboard:

- Manufacturer: Produsen motherboard"HP"
- Model: Model motherboard"8A4F"
- Bus Specs: Spesifikasi bus"PCI-Express 4.0 (16.0 GT/s)
- Chipset: Chipset motherboard"Alder Lake"
- Southbridge: Southbridge motherboard"Intel Alder Lake PCH"
- LPCIO: Informasi tentang LPCIO

- Bagian bawah:
- Informasi BIOS:
- Brand: Merek BIOS"AMI"
- Version: Versi BIOS"F.24"
- Date: Tanggal BIOS dibuat"10/26/2023"

![Screenshot 2024-02-29 151035](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/8ed5da14-a66f-440b-87dc-269a1daff7c8)
Bagian General:

- Type: Menunjukkan jenis memori yang digunakan"DDR4"
- Size: Menunjukkan jumlah memori yang terpasang"16 GB"
- Channel: Menunjukkan jumlah channel memori yang digunakan"2 x 64-bit"
- Mem Controller Freq.: Menunjukkan clock speed pengontrol memori"798.0 MHz"
- Uncore Frequency: Menunjukkan clock speed uncore"2693.4 MHz"

Bagian Timings:

- DRAM Frequency: Menunjukkan clock speed memori"1596.1 MHz"
- FSB:DRAM: Menunjukkan rasio antara FSB dan DRAM clock speed"1:12"
- CAS# Latency (CL): Menunjukkan latency CAS"22.0 clocks"
- RAS# to CAS# Delay (tRCD): Menunjukkan RAS# to CAS# delay"22 clocks"
- RAS# Precharge (tRP): Menunjukkan RAS# precharge"22 clocks"
- Cycle Time (tRAS): Menunjukkan cycle time"52 clocks"
- Bank Cycle Time (tRC): Menunjukkan bank cycle time"74 clocks"
- Command Rate (CR): Menunjukkan command rate"1T"

![Screenshot 2024-02-29 152215](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/13424448-c851-4013-900a-d7a738e19f69)
Informasi Memori:

- Slot Memori: #1
- Tipe: DDR4
- Ukuran Modul: 8 GB
- Produsen Modul: Micron Technology
- Minggu/Tahun: 21/22
- Manufaktur DRAM: Micron Technology
- Peringkat: Single
- Nomor Bagian: 8ATF1G64HZ-3G2R1
- Nomor Seri: 3803A235
- Tegangan: 1.20 V

- Slot Memori #2:
- Tipe: DDR4
- Ukuran Modul: 8 GB
- Produsen Modul: Micron Technology
- Minggu/Tahun: 09/23
- Manufaktur DRAM: Micron Technology
- Peringkat: Single
- Nomor Bagian: 8ATF1G64HZ-3G2R1
- Nomor Seri: 3EBAE82D
- Tegangan: 1.20 V

![Screenshot 2024-02-29 193014](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/cb1fcdbe-a88b-4c17-97c6-aacc107719d1)

Display Device Selection: Memungkinkan Anda memilih perangkat tampilan yang ingin Anda lihat informasinya
- GPU: Menunjukkan informasi tentang GPU, seperti nama, vendor, dan clock speed
- Name: "Intel(R) Iris(R) Xe Graphics"
- Board Manuf.: Menunjukkan nama pabrikan motherboard"Hewlett-Packard"
- Code Name: Menunjukkan nama kode CPU.
- Revision: Menunjukkan revisi CPU"C"
- Technology: Menunjukkan teknologi manufaktur CPU.

Clocks:
- GFX Core"1400.0 MHz

![Screenshot 2024-02-29 192239](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d4712dfc-4488-4896-b44f-ea8bf8a70202)

- GPU: Menunjukkan informasi tentang GPU, seperti nama, vendor, dan clock speed
- Name: "NVIDIA GeForce RTX 3050 Laptop Gpu"
- Board Manuf.: Menunjukkan nama pabrikan motherboard"Hewlett-Packard"
- Code Name: Menunjukkan nama kode CPU"GA107"
- Technology: Menunjukkan teknologi manufaktur CPU"8 nm"
- TDP: Menunjukkan Thermal Design Power (TDP) CPU"60.0W"
- Revision: Menunjukkan revisi CPU"A1"

Clocks:
- GFX Core: "1500.0" MHz"
- Memory: "5871.0 MHz"

Memory
- Size: "4 GBytes"
- Type: "GDDR6"
- Vendor: "Hynix"
- Bus Width: "128 bits"

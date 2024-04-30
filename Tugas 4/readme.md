# Tugas 4


## Daftar Tugas
- [Langkah siklus cpu](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%203#mind-map)
- [Peran Bahasa Pemrograman dan Compiler](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%203#langkah-siklus-cpu)
- [Install Debian dan Jalankan FLOPS-IOPS](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%203#pengertian-dan-peran-sistem-operasi)
- [Laporan praktikum sisop]()



## Langkah siklus cpu

![WhatsApp Image 2024-03-23 at 16 46 46_5b653f2c](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/80030fad-df33-4c51-a175-aa7809f9ad61)

## Peran Bahasa Pemrograman dan Compiler

**Bahasa pemrograman** dan **compiler** adalah dua elemen penting dalam dunia pemrograman yang saling terkait dan memiliki peran krusial dalam proses pengembangan perangkat lunak. Berikut penjelasan detailnya:

**Peran Bahasa Pemrograman:**

* **Menyediakan alat** bagi programmer untuk menulis instruksi yang dapat dipahami oleh komputer. Bahasa pemrograman memiliki struktur dan sintaks yang terorganisir, memungkinkan programmer untuk membuat kode yang mudah dibaca, dipahami, dan dipelihara.
* **Memungkinkan pembuatan berbagai jenis program**. Dengan bahasa pemrograman, programmer dapat membangun berbagai aplikasi, seperti aplikasi desktop, web, mobile, game, dan sistem tertanam.
* **Membantu memecahkan masalah dan mengembangkan solusi logis**. Bahasa pemrograman menyediakan kerangka kerja untuk mendefinisikan masalah, menganalisisnya, dan merancang solusi yang efektif.
* **Meningkatkan kemampuan berpikir logis dan problem solving**. Mempelajari dan menggunakan bahasa pemrograman melatih otak untuk berpikir terstruktur, analitis, dan sistematis,  

**Contoh Bahasa Pemrograman Populer:** Python, Java, C++, JavaScript, PHP, Go, dan R.

**Peran Compiler:**

* **Menerjemahkan kode bahasa pemrograman tingkat tinggi (seperti Python atau Java) menjadi kode mesin**. Kode mesin adalah bahasa yang dipahami dan dijalankan langsung oleh prosesor komputer.
* **Membuat program yang dapat dieksekusi**. Compiler menghasilkan file yang dapat dijalankan (executable file) yang berisi instruksi yang dapat dipahami dan dijalankan oleh sistem operasi.
* **Mengoptimalkan kode untuk meningkatkan performa dan efisiensi program**. Compiler dapat melakukan analisis dan optimasi kode untuk memastikan program berjalan dengan lancar dan menggunakan sumber daya komputer secara optimal.
* **Melakukan pemeriksaan untuk memastikan kode bebas dari kesalahan**. Compiler mendeteksi dan melaporkan kesalahan sintaks dan semantik dalam kode untuk membantu programmer menemukan dan memperbaikinya.

**Kesimpulan:**

Bahasa pemrograman dan compiler bekerja sama untuk menghasilkan perangkat lunak yang fungsional dan efisien. Bahasa pemrograman menyediakan alat bagi programmer untuk merancang dan menulis kode, sedangkan compiler menerjemahkan kode tersebut menjadi bahasa mesin yang dapat dijalankan oleh komputer.

**Tambahan:**

* **Jenis-jenis Bahasa Pemrograman:** Bahasa pemrograman dikategorikan berdasarkan tingkat abstraksinya. Bahasa pemrograman tingkat tinggi (seperti Python dan Java) lebih mudah digunakan, sedangkan bahasa pemrograman tingkat rendah (seperti C dan C++) lebih dekat dengan hardware dan lebih kompleks.
* **Jenis-jenis Compiler:** Compiler dikategorikan berdasarkan platform targetnya. Compiler native menerjemahkan kode ke dalam kode mesin untuk platform tertentu, sedangkan compiler cross-platform menerjemahkan kode ke dalam kode mesin untuk berbagai platform.
* **Alat-alat Pengembangan Lainnya:** Selain bahasa pemrograman dan compiler, berbagai alat pengembangan lain digunakan dalam proses pengembangan perangkat lunak, seperti interpreter, debugger, dan linker.


## Install Debian dan Jalankan FLOPS-IOPS

$ make
$ make clean
$ sudo make install
$ sudo make uninstall
![Screenshot 2024-03-17 203254](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/428361b7-4dbc-4ffb-9b18-58f86082a626)

$ iops64 $(nproc)
![Screenshot 2024-03-17 203407](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/8076ea82-1c7e-44af-b874-1d7e5956109d)

$ flops64 $(nproc)
![Screenshot 2024-03-17 204129](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d520bb38-de0b-4c61-9550-4e115413befc)

Kesimpulan tentang IOPS dan FLOPS
FLOPS (Floating-point Operations Per Second) dan IOPS (Input/Output Operations Per Second) adalah metrik penting untuk mengukur kemampuan komputer, namun keduanya mengukur aspek yang berbeda:

- FLOPS adalah parameter untuk menilai kecepatan proses komputasi floating-point oleh CPU. Semakin tinggi nilai FLOPS, semakin efisien CPU dalam menangani perhitungan matematika yang rumit, seperti yang sering diperlukan dalam bidang seperti simulasi rekayasa, pembelajaran mesin, dan komputasi ilmiah.

- Sementara itu, IOPS adalah parameter untuk mengukur kinerja penyimpanan, seperti hard disk drive atau solid state drive, dalam melakukan operasi transfer data. Semakin tinggi nilai IOPS, semakin cepat penyimpanan dalam membaca dan menulis data, yang pada gilirannya memengaruhi kinerja keseluruhan sistem saat mengakses file dan aplikasi.

Hubungan antara IOPS dan FLOPS:

Pengujian menunjukkan hubungan positif antara IOPS dan FLOPS. Komputer yang dilengkapi dengan CPU yang lebih kuat, yang biasanya memiliki FLOPS yang lebih tinggi, cenderung memiliki kinerja penyimpanan yang lebih baik, yang tercermin dalam nilai IOPS yang lebih tinggi. Namun, penting untuk dicatat bahwa:

Hubungan ini tidak selalu konsisten. Ada faktor lain yang juga memengaruhi kinerja, seperti jenis penyimpanan dan konfigurasi sistem.
Peningkatan kapasitas RAM tidak selalu memberikan dampak yang signifikan terhadap FLOPS dan IOPS. RAM lebih berperan dalam menjalankan program secara keseluruhan daripada perhitungan individu atau transfer data.
Kesimpulan:

FLOPS dan IOPS memberikan gambaran tentang kemampuan komputasi dan transfer data pada sebuah komputer.
Saat memilih komputer yang sesuai, penting untuk mempertimbangkan jenis tugas yang akan dilakukan. Aplikasi yang mengharuskan komputasi berat memerlukan FLOPS yang tinggi, sementara aplikasi yang sering mengakses file besar membutuhkan IOPS yang tinggi.
Sebaiknya, komputer memiliki keseimbangan yang baik antara FLOPS dan IOPS untuk mencapai performa optimal.

## Laporan praktikum sisop

![LAPORAN_SISTEM_OPERAS_1-01 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/2fcd9a54-7c92-4a17-986e-cae52cd9b732)
![LAPORAN_SISTEM_OPERAS_1-02 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/6bf4a345-4037-4b15-963a-785b953256bf)
![LAPORAN_SISTEM_OPERAS_1-03 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/2f5ee0d5-15ba-4b27-b203-9d409b55340a)
![LAPORAN_SISTEM_OPERAS_1-04 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d0970c42-10eb-4ea6-a9e2-a5bab1f1c784)
![LAPORAN_SISTEM_OPERAS_1-05 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/e509fb35-198b-4607-a73d-204e2447c41f)
![LAPORAN_SISTEM_OPERAS_1-06 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/fbab55e0-becd-463b-87fd-016c5b0383cc)
![LAPORAN_SISTEM_OPERAS_1-07 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/4fd8f499-93fd-4b07-bf6a-e36a22ef5c5f)
![LAPORAN_SISTEM_OPERAS_1-08 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/a6d5dfb7-f5b4-4934-a792-70ca7d32bed4)
![LAPORAN_SISTEM_OPERAS_1-09 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d9093494-f76d-4fe2-9318-bd28d929bfa6)
![LAPORAN_SISTEM_OPERAS_1-10 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/8ab25221-cb5c-4819-ba3f-6650cd507aef)
![LAPORAN_SISTEM_OPERAS_1-11 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/88e1678f-0ebb-4db2-ae1c-3242d5809ee8)
![LAPORAN_SISTEM_OPERAS_1-12 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/b7325dc7-93f2-41d7-8b53-51f69f1fb01b)
![LAPORAN_SISTEM_OPERAS_1-13 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/ad2b5464-8a30-4bd9-b147-dc9a7f353f57)
![LAPORAN_SISTEM_OPERAS_1-14 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/cfc85710-974a-4b49-9267-07dfd5d5937c)
![LAPORAN_SISTEM_OPERAS_1-15 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/126fa31e-b99c-4501-91f4-50942434f391)
![LAPORAN_SISTEM_OPERAS_1-16 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/0c48bd5a-2f0a-4d0d-a4e4-00d653af7f66)
![LAPORAN_SISTEM_OPERAS_1-17 1](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d962cb59-b3fc-4a2f-9e00-c7769b4cf5cf)


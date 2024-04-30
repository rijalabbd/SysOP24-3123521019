# Tugas 3


## Daftar Tugas
- [Mind Map]()
- [Perbedaan BIOS dan UEFI](https://github.com/rijalabbd/SysOP24-3123521019/blob/main/Tugas%203/readme.md#langkah-siklus-cpu)


## Mind map
![Mind map sejarah OS](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/d7b85f36-8da8-4597-a27a-a52cf72913e2)

![INGLES](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/1e76b626-c0c4-42f0-8b2d-2694dd213ba8)


## Perbedaan BIOS dan UEFI
Baik BIOS maupun UEFI adalah firmware yang berperan dalam tahap awal booting komputer, namun keduanya memiliki perbedaan mendasar. Berikut penjelasannya:

**BIOS (Basic Input/Output System):**

* **Arsitektur:** 16-bit, membatasi kemampuannya untuk menangani perangkat keras modern secara optimal.
* **Antarmuka:** Biasanya berbasis teks, kurang intuitif dan penggunaannya terbatas.
* **Booting:** Proses booting umumnya lebih lambat dibandingkan UEFI.
* **Tipe Partisi:** Mendukung partisi MBR (Master Boot Record), yang memiliki keterbatasan kapasitas penyimpanan (maksimum 2TB per disk).
* **Keamanan:** Fitur keamanan terbatas.

**UEFI (Unified Extensible Firmware Interface):**

* **Arsitektur:** 32-bit atau 64-bit, memungkinkan penanganan perangkat keras modern secara lebih efisien.
* **Antarmuka:** Biasanya berbasis grafis (GUI), lebih user-friendly dan menawarkan fitur pengaturan yang lebih luas.
* **Booting:** Proses booting umumnya lebih cepat dibandingkan BIOS.
* **Tipe Partisi:** Mendukung partisi GPT (GUID Partition Table), yang tidak memiliki batasan kapasitas penyimpanan seperti MBR.
* **Keamanan:** Fitur keamanan lebih baik, seperti Secure Boot yang membantu mencegah booting dari perangkat yang tidak sah.

**Tabel Perbandingan:**

| Fitur                 | BIOS                               | UEFI                                 |
|------------------------|------------------------------------|-----------------------------------------|
| Arsitektur             | 16-bit                             | 32-bit atau 64-bit                    |
| Antarmuka             | Teks                                | Grafis (GUI)                          |
| Booting                 | Lambat                               | Lebih cepat                           |
| Tipe Partisi           | MBR (terbatas 2TB)                   | GPT (kapasitas tak terbatas)            |
| Keamanan               | Terbatas                             | Lebih baik (Secure Boot)               |



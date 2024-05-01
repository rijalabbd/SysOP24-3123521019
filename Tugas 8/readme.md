## Swapping dan Paging

Swapping dan paging adalah dua teknik manajemen memori yang digunakan dalam sistem operasi untuk mengatasi keterbatasan memori fisik. Memori fisik adalah memori yang dapat diakses langsung oleh CPU. 

**Swapping**

Swapping melibatkan memindahkan proses yang tidak aktif dari memori fisik ke disk swap. Disk swap adalah ruang penyimpanan pada disk yang digunakan untuk menyimpan proses yang tidak aktif. Ketika proses perlu diaktifkan kembali, proses tersebut dimuat kembali dari disk swap ke memori fisik.

**Paging**

Paging melibatkan membagi memori fisik menjadi halaman-halaman kecil yang berukuran sama. Setiap proses dialokasikan sejumlah halaman dalam memori fisik. Ketika proses perlu mengakses memori, alamat memori virtualnya diterjemahkan ke alamat memori fisik yang sesuai menggunakan tabel halaman.

**Perbedaan Swapping dan Paging**

| Fitur | Swapping | Paging |
|---|---|---|
| Unit alokasi memori | Seluruh proses | Halaman |
| Granularitas | Kasar | Halus |
| Overhead | Tinggi | Rendah |
| Penggunaan memori | Lebih efisien untuk proses besar | Lebih efisien untuk proses kecil |
| Kinerja | Lebih lambat | Lebih cepat |


**Kesimpulan**

Swapping dan paging adalah dua teknik manajemen memori yang penting untuk mengatasi keterbatasan memori fisik. Swapping lebih baik untuk proses besar yang tidak aktif untuk waktu yang lama, sedangkan paging lebih baik untuk proses kecil yang sering aktif dan tidak aktif. 



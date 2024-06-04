## Latihan

**4.1 Berikan tiga contoh pemrograman di mana multithreading memberikan kinerja yang lebih baik daripada solusi single-threaded.**

Berikut adalah tiga contoh penerapan multithreading yang menunjukkan performa yang lebih baik dibandingkan solusi single-threaded:

1. **Server Web:** Bayangkan sebuah server web yang menerima banyak permintaan secara bersamaan. Dengan multithreading, setiap permintaan dapat ditangani oleh thread terpisah, memungkinkan server untuk memproses beberapa permintaan secara paralel, meningkatkan kecepatan dan responsivitas.

2. **Aplikasi Paralel:** Pertimbangkan aplikasi komputasi intensif seperti perkalian matriks. Multithreading memungkinkan pembagian matriks menjadi bagian-bagian kecil yang dikerjakan oleh thread berbeda secara simultan, menyelesaikan operasi secara signifikan lebih cepat dibandingkan pendekatan single-threaded.

3. **Program GUI Interaktif:** Pada program seperti debugger, multithreading dapat meningkatkan performa dengan menjalankan tugas secara paralel. Satu thread dapat memantau input pengguna, thread lain menangani aplikasi yang sedang berjalan, dan thread ketiga memonitor kinerja, menghasilkan pengalaman pengguna yang lebih mulus dan responsif.

**4.2 Apa dua perbedaan antara thread tingkat pengguna dan thread tingkat kernel? Dalam kondisi apa satu jenis lebih baik dibandingkan jenis lainnya?**

Berikut adalah dua perbedaan utama antara thread tingkat pengguna dan kernel:

1. **Visibilitas Kernel:** Thread tingkat pengguna tidak terlihat oleh kernel, sedangkan thread kernel diketahui dan dikelola oleh kernel secara langsung.

2. **Penjadwalan:** Pada sistem dengan pemetaan M:1 atau M:N, thread pengguna dijadwalkan oleh pustaka thread, sedangkan thread kernel dijadwalkan oleh kernel. Thread kernel memiliki kontrol dan prioritas yang lebih tinggi.

**Kapan Menggunakan Masing-masing Jenis Thread:**

* **Thread Tingkat Pengguna:** Digunakan untuk aplikasi yang tidak memerlukan kontrol kernel yang ketat dan ingin menghindari overhead kernel. Cocok untuk tugas komputasi paralel yang tidak memerlukan sinkronisasi antar thread yang kompleks.
* **Thread Kernel:** Digunakan untuk aplikasi yang membutuhkan kontrol kernel, sinkronisasi antar thread yang kompleks, atau akses ke sumber daya kernel. Cocok untuk aplikasi real-time dan sistem yang membutuhkan kontrol presisi atas thread.

**4.3 Jelaskan tindakan yang diambil oleh kernel untuk beralih konteks antar thread tingkat kernel**

Saat beralih konteks antar thread kernel, kernel melakukan langkah-langkah berikut:

1. **Penyimpanan Register:** Nilai register CPU dari thread yang dialihkan disimpan ke dalam memori.

2. **Pemulihan Register:** Register CPU dari thread baru yang dijadwalkan dimuat dari memori.

3. **Penyesuaian Struktur Data:** Struktur data kernel yang terkait dengan thread diperbarui untuk mencerminkan peralihan konteks.

**4.4 Sumber daya apa yang digunakan saat thread dibuat? Apa perbedaannya dengan yang digunakan saat proses dibuat?**

Pembuatan thread umumnya membutuhkan lebih sedikit sumber daya dibandingkan pembuatan proses karena ukuran thread lebih kecil:

* **Proses:** Membutuhkan alokasi blok kontrol proses (PCB) yang besar, termasuk peta memori, daftar file terbuka, dan variabel lingkungan. Alokasi peta memori umumnya memakan waktu paling lama.
* **Thread:** Membutuhkan alokasi struktur data yang lebih kecil untuk menyimpan set register, tumpukan, dan prioritas.

**4.5 Asumsikan bahwa sistem operasi memetakan thread tingkat pengguna ke kernel menggunakan model banyak ke banyak dan pemetaan dilakukan melalui LWP. Selain itu, sistem ini memungkinkan pengembang membuat thread real-time untuk digunakan dalam sistem real-time. Apakah perlu untuk mengikat thread real-time ke LWP? Menjelaskan**

Dalam sistem yang menggunakan model banyak-ke-banyak untuk memetakan thread pengguna ke kernel dengan LWP, mengikat thread real-time ke LWP sangat penting:

* **Alasan:** Pengaturan waktu sangat penting untuk aplikasi real-time. Jika thread real-time tidak terikat ke LWP, ia mungkin harus menunggu untuk dilampirkan sebelum dijalankan, berpotensi menyebabkan penundaan yang tidak dapat diterima.
* **Manfaat:** Mengikat thread real-time ke LWP memastikan thread dapat berjalan dengan penundaan minimal setelah dijadwalkan, memenuhi persyaratan waktu nyata aplikasi.

**Kesimpulan**

Multithreading menawarkan banyak keuntungan dibandingkan solusi single-threaded, terutama untuk aplikasi yang membutuhkan pemrosesan paralel, responsivitas, dan skalabilitas. Memahami perbedaan antara thread tingkat pengguna dan kernel, serta mekanisme context switching kernel, penting untuk memilih jenis thread yang tepat dan mengoptimalkan kinerja aplikasi. 


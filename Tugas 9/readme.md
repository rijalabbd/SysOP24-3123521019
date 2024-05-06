## Menerjemahkan Artikel

printf (“HELLO WORD!”); Bagian terbaik tentang pemrograman komputer adalah semua masalahnya berhubungan dengan dunia nyata; program dan perangkat lunak komputer adalah solusi untuk memenuhi kebutuhan sehari-hari Anda dan saya mulai dari pemesanan makanan online, belanja, media sosial, pemesanan tiket, dan lainnya!

Jadi, Misalkan Anda adalah pemilik toko Roti bernama “Bakes and Bytes”; dan kamu bisa membuat maksimal 50 kue karena kamu belum mempunyai oven yang besar. Sekarang, Anda memiliki beberapa pelanggan untuk membelinya, tapi mari kita pertimbangkan hanya satu pelanggan. Toko roti Anda canggih dan karenanya memiliki sistem manajemen yang hebat seperti kode yang diberikan.

//Reference: https://en.wikipedia.org/wiki/Producer%E2%80%93consumer_problem


int OVEN_SIZE = 50;
int cakes = 0;

procedure baker()
{
while (true)
{
cakes = bake_cake();


```
if (cakes == OVEN_SIZE)
{
  // Do something (possibly bake a cake)
}
sleep();

putCakeInDisplay(cake);
cakes = cakes + 1;

if (cakes == 1)
{
  // Do something (possibly wake up a consumer)
}
wakeup(consumer);
```

}

procedure customer()
{
while (true)
{


```
if (cakes == 0)
{

}                            sleep();

item
cakes cakes 1;
-
takeCakeFromBakery();

if (cakes == OVEN_SIZE - 1)
{

}                                      wakeup (baker);

}  buy_cakes (cakes);
```


**Situasi:**

Toko roti memiliki persediaan kue yang terbatas. Ketika persediaan habis (kue == 0), toko roti akan memberitahukan pelanggan untuk menunggu ("sleep()") hingga oven penuh kembali. 

Pembuat roti terus membuat kue baru sampai oven penuh (kue != 50). Ketika oven penuh, pembuat roti akan "tidur" sampai pelanggan membeli kue dan persediaan berkurang (kue != 50). 

Namun, terdapat beberapa kendala dalam sistem ini:

1. **Konflik antara Pembuat Roti dan Pelanggan:** Pembuat roti memproduksi kue, sementara pelanggan ingin membelinya. Pelanggan mungkin mengira kue sudah siap, sedangkan pembuat roti masih memproduksi. Hal ini dapat menyebabkan kekacauan.

2. **Ketidakcocokan Waktu:** Pelanggan melihat persediaan habis dan ingin tidur. Pembuat roti mungkin memproduksi kue baru saat pelanggan hendak tidur. Ketika kue baru tersedia, toko roti memberitahukan pelanggan untuk "bangun!". 

Tetapi, karena pelanggan ingin tidur, mereka tidak akan merespon pesan "bangun!". Hal ini terjadi karena kurangnya sinkronisasi antara pembuat roti dan pelanggan.

3. **Ketidakseimbangan Produksi dan Konsumsi:** Pembuat roti terus memproduksi kue hingga oven penuh (50 kue), meskipun tidak ada pelanggan yang membeli. Ketika persediaan kue mencapai satu (kue == 1), pelanggan terbangun, tetapi pembuat roti terus memproduksi kue. Hal ini menyebabkan persediaan kue tidak pernah mencapai satu dan pelanggan terus tertidur.

Situasi ini menggambarkan masalah **Produsen-Konsumen**, di mana terdapat ketidakseimbangan antara produksi dan konsumsi. 

**Solusi:**

Diperlukan solusi untuk mengatasi masalah sinkronisasi dan ketidakseimbangan antara pembuat roti dan pelanggan. Solusi ini dapat berupa mekanisme antrian, semaphore, atau mekanisme lainnya yang memungkinkan komunikasi dan koordinasi yang lebih baik antara pembuat roti dan pelanggan.

![Screenshot 2024-05-06 195214](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/1d53de49-f566-4fd0-affc-e0a0329a1126)

## Penjelasan Masalah Produsen dan Konsumen 

**Masalah Produsen dan Konsumen** adalah masalah sinkronisasi di mana terdapat produsen yang memproduksi item dan konsumen yang mengkonsumsinya. Masalah ini muncul ketika terdapat buffer dengan ukuran terbatas yang digunakan untuk menampung item yang diproduksi.

**Solusi**

Solusi untuk masalah ini adalah dengan menggunakan **semaphore**. Semaphore adalah variabel yang digunakan untuk mengontrol akses ke sumber daya bersama oleh beberapa proses. Dalam kasus ini, semaphore digunakan untuk memastikan bahwa hanya satu produsen yang dapat memproduksi item ke dalam buffer pada satu waktu, dan hanya satu konsumen yang dapat mengambil item dari buffer pada satu waktu.

**Contoh Implementasi**

Berikut adalah contoh implementasi masalah produsen dan konsumen dalam bahasa C:

**Main Function**

```c
#include<stdio.h>
#include<pthread.h>
#include<semaphore.h>
#define SHARED 1
void *Producer(); // Make Declaration of Producer
void *Consumer(); // Make Declaration of Consumer
sem_t empty, full; //Declare semaphores to be used
int data; // data variable

int main()
{
pthread_t ptid, ctid; // Line 1
printf("\nMain Started");
sem_init(&empty, SHARED, 1); // Line 2
sem_init(&full, SHARED, 0); // Line 3
sem_init(&sm, SHARED, 1);// Line 4
pthread_create(&ptid,NULL,Producer,NULL); // Line 5
pthread_create(&ctid,NULL,Consumer,NULL); // Line 6
pthread_join(ptid,NULL); // Line 7
pthread_join(ctid,NULL); // Line 8
printf("\nMain done\n");
}
```

**Fungsi Produsen**

```c
void *Producer()
{
//ITEM PRODUCED...
int produced;
printf("\nProducer created");
printf("\nProducer id is %ld\n",pthread_self()); //print thread id
for(produced=0;produced<100;produced++)
{
sem_wait(&empty);
// LOCK-starts
sem_wait(&sm);
//CRITICAL SECTION STARTS
data=produced;
//CRITICAL SECTION ENDS
sem_post(&sm);
//LOCK-ends
sem_post(&full);
printf("\nProducer: %d",data);
}
}
```

**Fungsi Konsumen**

```c
void *Consumer()
{
int consumed, total=0;
printf("\nConsumer created\n");
printf("\nConsumer id is %ld\n",pthread_self());
for(consumed=0;consumed<100;consumed++)
{
sem_wait(&full);
//LOCK-starts
sem_wait(&sm);
//CRITICAL SECTION STARTS
total=total+data;
//CRITICAL SECTION ENDS
sem_post(&sm);
//LOCK-ends
sem_post(&empty);
printf("\nConsumed: %d",data);
}
printf("\nThe total of 100 iterations is %d\n",total);
}
```

**Penjelasan**

* **Main function**
    * Membuat thread produsen dan konsumen
    * Inisialisasi semaphore
    * Menunggu thread produsen dan konsumen selesai
    * Menampilkan pesan "Main done"

* **Fungsi Produsen**
    * Menghasilkan item
    * Menunggu semaphore empty
    * Menunggu semaphore 'sm' untuk memastikan tidak ada konsumen yang mengakses buffer
    * Memasukkan item ke dalam buffer
    * Meningkatkan semaphore 'sm'
    * Meningkatkan semaphore full
    * Menampilkan pesan "Producer: %d"

* **Fungsi Konsumen**
    * Mengambil item dari buffer
    * Menunggu semaphore full
    * Menunggu semaphore 'sm' untuk memastikan tidak ada produsen yang mengakses buffer
    * Mengurangi item dari buffer
    * Meningkatkan semaphore 'sm'
    * Meningkatkan semaphore empty
    * Menampilkan pesan "Consumed: %d"

**Kesimpulan**

Masalah produsen dan konsumen adalah masalah sinkronisasi klasik yang dapat dipecahkan dengan menggunakan semaphore. Kode yang saya berikan di atas adalah contoh implementasi masalah produsen dan konsumen dalam bahasa C. Kode ini telah diparafrase untuk membuatnya lebih mudah dipahami.

# Tugas 5

## Daftar Tugas
- [Cloning Repository](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%205#cloning-repository)
- [fork01](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%205#fork01)
- [fork02](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%205#fork02)
- [fork03](https://github.com/zakwanaraffi/SysOP24-3123521030/tree/main/Tugas%205#fork03)

## Cloning Repository
Buat tulisan tentang konsep fork dan implementasinya dengan menggunakan bahasa pemrograman C! (minimal 2 paragraf disertai dengan gambar)
Akses dan clonning repo : https://github.com/ferryastika/operatingsystem.git
Deskripsikan dan visualisasikan pohon proses hasil eksekusi dari kode program fork01.c, fork02.c, fork03.c,
![Screenshot 2024-04-22 205307](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/e72b84e4-2c31-4f1b-b4a5-097f5ca3da47)

Langkah pertama adalah masuk ke superuser dengan mengetikkan su -, kemudian ketikkan sudo apt install gcc g++. Jika mengalami kesalahan atau tidak memiliki akses karena tidak terdaftar dalam file sudoers, Anda dapat menambahkan pengguna ke grup sudo dengan menggunakan perintah sudo usermod -aG sudo (username). Sebagai contoh, jalankan perintah sudo usermod -aG sudo rijal untuk menambahkan pengguna dengan nama "rijal" ke grup "sudo". Setelah perintah ini dieksekusi, pengguna "rijal" akan memiliki akses sudo di sistem tersebut. 

Setelah menambahkan pengguna ke grup sudo, dapat kembali mencoba menginstal gcc dan g++ dengan mengetikkan sudo apt install gcc g++
## fork01
Perintah sudo apt install gcc g++ digunakan untuk menginstal compiler GNU untuk bahasa pemrograman C dan C++ di sistem operasi berbasis Debian atau Ubuntu. gcc adalah compiler untuk bahasa pemrograman C, sedangkan g++ adalah compiler untuk bahasa pemrograman C++.

![Screenshot 2024-04-22 205004](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/0c81b619-20f9-473e-945c-a41ecbdff6e7)
![Screenshot 2024-04-22 223415](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/838ba305-1f19-43de-8118-af559820e10b)
![Screenshot 2024-04-22 223545](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/4bb3efb2-d4e6-47a4-9ca1-8b2c5e6635bc)


Berikut ini kode yang telah disesuaikan:

```cpp
#include <iostream>
#include <sys/types.h>
#include <unistd.h>

int main(void) {
    pid_t mypid;
    uid_t myuid;
    for (int i = 0; i < 3; i++) {
        mypid = getpid();
        std::cout << "I am process " << mypid << std::endl;
        std::cout << "My parent process ID is " << getppid() << std::endl;
        std::cout << "The owner of this process has UID " << getuid() << std::endl;
        sleep(3);
    }
    return 0;
}
```

Setelah mengetikkan kode tersebut di dalam berkas `fork01.cpp`, Kita dapat menyimpannya dengan menekan `Ctrl + X`, lalu pilih `Y` untuk menyimpan perubahan, dan tekan `Enter`.

Kemudian, Kita dapat mengompilasi program tersebut dengan perintah:

```
g++ fork01.cpp -o fork01.exe
```

Perintah ini akan mengkompilasi program C++ yang disebut "fork01.cpp" menggunakan compiler g++ dan memberikan output dengan nama "fork01.exe".

Terakhir, jalankan program dengan perintah:

```
./fork01.exe
```
## fork02
![Screenshot 2024-04-22 224225](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/e9fdb3de-1df5-45ee-8e24-e564c70577c0)
![Screenshot 2024-04-22 224458](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/b6a056b0-9070-4b79-a766-8b5efbc0c228)

Program di atas melakukan proses forking secara berulang sebanyak lima kali. Setiap kali proses forking dilakukan, program mencatat ID proses (PID) dari setiap proses yang dihasilkan. Jika terdapat PID yang berulang, itu menandakan bahwa proses utama telah melakukan forking beberapa kali, menghasilkan beberapa proses anak dengan PID yang sama.

## fork03
![Screenshot 2024-04-22 224833](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/8a8531ea-058a-4429-bbe0-845ae24a016e)
![Screenshot 2024-04-22 224939](https://github.com/rijalabbd/SysOP24-3123521019/assets/141767343/9f4f7b90-22e7-431d-9f1f-e569742da3fd)



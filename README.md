# TUGAS-PRAKTIKUM-4-SISTEM-OPERASI

**NAMA : Miki Purnawan**

**NIM : 09011282328122**

**KELAS : SK3B**

**TUGAS PRAKTIKUM 5 SISTEM OPERASI TENTANG JOB CONTROL**

1. Eksekusi seluruh profile yang ada :
   
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 

echo “Profile dari /etc/profile” 

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : 

/home/stD02001/.bash_profile 

/home/. stD02001/.bash_login 

/home/mahasiswa/.profile 

/home/mahasiswa/.bashrc 

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : 

echo “Profile dari .bash_profile” 

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. 

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 

$ su mahasiswa 

$ exit 

kemudian gunakan opsi – sebagai berikut : 

$ su – mahasiswa 

$ exit 

Jelaskan perbedaan kedua utilitas tersebut.

Jawab :

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 

echo “Profile dari /etc/profile” 

![tugas so 5 1a](https://github.com/user-attachments/assets/4aaa5326-97c4-4acd-8ae4-836a263b3668)

Pertama-tama buat edit isi file dari profile yang berada di direktori /etc/ dengan cara nano /etc/profile, kemudian ketikkan echo "Profile dari /etc/profile", pesan echo ini akan muncul setiap kali kita akan login ke terminal

![tugas so 5 1aaa](https://github.com/user-attachments/assets/7a6bbf09-d5a2-415e-b1d8-484d1008d4b9)

setelah berhasil mengedit isi file dari /etc/profile, coba cek menggunakan source apakah ada perubahan, seharusnya jika sudah benar maka pesan echo yang baru kita masukkan ke file akan muncul seperti gambar di atas

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : 

/home/stD02001/.bash_profile 

/home/. stD02001/.bash_login 

/home/mahasiswa/.profile 

/home/mahasiswa/.bashrc 

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : 

echo “Profile dari .bash_profile” 

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.

Untuk yang ini dikarenakan file .bash_login dan .bash_profile tidak ada, jadi saya akan membuat sendiri file tersebut di direktori /home/miki-purnawan/ (miki-purnawan adalah username saya) :

1. nano .bash_profile, setelah menggunakan command nano, ketikkan echo "Profile dari .bash_profile" kemudian tekan ctrl + x untuk menyimpan isi file

![tugas so 5 1b](https://github.com/user-attachments/assets/f4275634-332e-4940-b132-991090b82294)

2. nano .bash_login, ketikkan echo "Profile dari .bash_login" kemudian tekan ctrl + x untuk menyimpan isi file nya

![tugas so 5 1bb](https://github.com/user-attachments/assets/7b8f15e2-048d-42ca-8553-92dedbc70d9b)

3. nano .bashrc, ketikkan echo "Profile dari .bashrc" di bagian atas setelah tulisan berwarna biru seperti yang di gambar kemudian simpan perubahan menggunakan ctrl + x

![tugas so 5 1bbb](https://github.com/user-attachments/assets/cb509fde-94ca-4dca-adcd-82053b6c6d14)

4. nano .profile, sama seperti nano.bashrc, ketikkan echo "Profile dari .profile" dan simpan perubahan

![tugas so 5 1bbbb](https://github.com/user-attachments/assets/04a5197e-dc1d-4727-a06b-205cce71d71b)

Setelah mengedit isi 4 file tersebut, coba gunakan command source seperti gambar di bawah ini apakah ada perubahan 

![tugas so 5 1bbbbb](https://github.com/user-attachments/assets/bb30d89a-b561-4a8e-a849-9567577f05b7)

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 

$ su mahasiswa 

$ exit 

kemudian gunakan opsi – sebagai berikut : 

$ su – mahasiswa 

$ exit 

Jelaskan perbedaan kedua utilitas tersebut.

![tugas so 5 1c](https://github.com/user-attachments/assets/60c0d88d-0122-410d-a049-58fc4ef444cd)

Perbedaan antara su dan su - adalah bahwa saat menggunakan su, jika kita berpindah ke akun bernama miki-purnawan, kita tetap berada di terminal yang sama dan di direktori yang sama. Namun, saat menggunakan su -, kita benar-benar berpindah ke lingkungan pengguna baru, seolah-olah kita masuk sebagai pengguna miki-purnawan dari awal. Ini berarti kita juga berpindah ke direktori home pengguna tersebut, dan semua pengaturan serta variabel lingkungan pengguna miki-purnawan dimuat. Dengan kata lain, su hanya mengganti identitas pengguna tanpa mengubah lokasi, sementara su - menciptakan sesi baru dengan semua pengaturan pengguna baru.

2. Prompt String (PS)
   
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell 

PS1='>' 

export PS1

b. Eksperimen hasil PS1 :

$ PS1=“\! > “ 

69 > PS1=”\d > “ 

Mon Sep 23 > PS1=”\t > “ 

10:10:20 > PS1=”Saya=\u > “ 

Saya=mahasiswa > PS1=”\w >” 

~ > PS1=\h >” 

Jawab :

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell 

PS1='>' 

export PS1

![tugas so 5 2a](https://github.com/user-attachments/assets/c5943cc9-9cfa-4164-b797-2445ae43bc5b)

Kita edit file .bash_profile menggunakan prompt nano .bash_profile, lalu ketikkan "PS1='>'" dan "export PS1" 

![tugas so 5 2aa](https://github.com/user-attachments/assets/aacc719f-c7c6-42d2-84a6-e3f12ca47549)

Setelah mengedit isi file .bash_profile coba cek menggunakan source .bash_profile untuk melihat apakah tanda $ berubah menjadi > sesuai dengan PS1='>'

b. Eksperimen hasil PS1 :

$ PS1=“\! > “ 

69 > PS1=”\d > “ 

Mon Sep 23 > PS1=”\t > “ 

10:10:20 > PS1=”Saya=\u > “ 

Saya=mahasiswa > PS1=”\w >” 

~ > PS1=\h >” 

![Screenshot 2024-09-21 123407](https://github.com/user-attachments/assets/8a19c583-5834-42fd-aea6-04a7d446d630)

Penjelasan :

a. PS1=“\! > “ : Command ini untuk mengetahui berapa banyak history command prompt yang sudah kita gunakan dalam terminal dengan menjadikan output dari ! sebagai prompt shell sehingga prompt shell yang awalnya miki-purnawan@Miki-Purnawan-VirtualBox:~$ menjadi 315> saja (315 adalah history command prompt yang sudah digunkakan dan > hanyalah simbol, sama seperti $, # dan lain lain)

b. 315>PS1="\d>" : ini untuk menampilkan hari, bulan dan tanggal yang kemudian hasil output nya dijadikan prompt shell 

c. Sat Sep 21>PS1="\t>" : ini untuk menampilkan waktu dengan format jam, menit dan detik kemudian hasil output nya menjadi prompt shell

d. 12:33::23>PS1="miki-purnawan=\u>" : ini berfungsi untuk menampilkan username yang digunakan kemudian dijadikan sebagai prompt shell bersamaan dengan miki-purnawan= sehingga prompt shell nya adalah miki-purnawan=miki-purnawan>

e. miki-purnawan=miki-purnawan>PS1="\w>" : ini berfungsi untuk menampilkan direktori saat ini lalu dijadikan prompt shell, karena saya berada di direktori ~ maka dari itulah prompt shell nya berubah menjadi ~>

f. ~>PS1="\h>" : ini berfungsi untuk menampilkan nama host atau nama komputer kemudian hasil output nya dijadikan teks statis di prompt shell 

3.  Logout  

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout :

Echo “Terima kasih atas sesi yang diberikan”  

Sleep 5  

clear  

Jawab :

Edit file pada .bash_logout dan ketikkan :

Echo “Terima kasih atas sesi yang diberikan”  

Sleep 5  

clear 

![so 5 no 3a](https://github.com/user-attachments/assets/8b415e87-0493-4a85-ada4-434a8da2ad81)

Setelah mengedit isi file dari .bash_logout, coba lah untuk log out dengan cara exit untuk melihat apakah ada pesan echo kemudian sistem terminal akan sleep selama 5 detik dan setelah itu akan mengeksekusi command terminal yang sudah kita masukkan di dalam file .bash_logout. Contoh output nya seperti gambar di bawah ini (jika pesan echo tidak muncul setelah mengedit isi file .bash_logout, cobla untuk login menggunakan su - "username" kemudian logout kembali)

![so 5 no 3aa](https://github.com/user-attachments/assets/8560fa93-b889-4565-a669-f6cf2f0a43fe)

4. Bash script  

a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :  

**1. p1.sh**  

#! /bin/bash  

echo “Program p1”  

ls –l  

**p2.sh**

#! /bin/bash  

echo “Program p2”  

who  

**p3.sh**  

#! /bin/bash  

echo “Program p3”  

ps x  

b.  Jalankan script tersebut sebagai berikut :  

$  ./p1.sh ; ./p3.sh ; ./p2.sh  

$  ./p1.sh &  

$  ./p1.sh & ./p2.sh & ./p3.sh &  

$  ( ./p1.sh ; ./p3.sh ) & 

Jawab :

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

**1. p1.sh**

![so 5 no 4a](https://github.com/user-attachments/assets/41a77a70-016e-4481-83e1-51d3f4ad3549)

Buat file bernama p1.sh dengan menggunakan nano p1.sh kemudian masukkan kode sesuai dengan yang di soal kemudian simpan dengan menekan ctrl + x

**2. p2.sh**

![so 5 no 4aa](https://github.com/user-attachments/assets/d95b6a37-c3cb-476c-98a9-77488b58ceff)

Buat file bernama p2.sh dengan menggunakan nano p1.sh kemudian masukkan kode sesuai dengan yang di soal kemudian simpan dengan menekan ctrl + x

**3. p3.sh**

![so 5 no 4aaa](https://github.com/user-attachments/assets/8a87bc1c-8e8b-4a73-b783-b0c932ab1ffa)

Buat file bernama p3.sh dengan menggunakan nano p1.sh kemudian masukkan kode sesuai dengan yang di soal kemudian simpan dengan menekan ctrl + x. Setelah membuat 3 file bash tersebut, ubah terlebih dahulu izin akses file nya agar bisa di eksekusi, caranya chmod +x p1.sh p2.sh p3.sh

**b. Jalankan script**

a. ./p1.sh ; ./p3.sh ; ./p2.sh

![so 5 no 4b](https://github.com/user-attachments/assets/f8c27b99-1a13-4584-a9d9-d44358afeef7)

Command ini berfungsi untuk mengeksekusi file p1, p2 dan p3 secara bergantian jadi pertama eksekusi p1.sh sampai selesai terus p3.sh sampai selesai dan p2.sh (p1.sh  berisi echo dan ls -l, p2.sh berisi echo dan who dan p3.sh berisi ps x)

b. ./p1.sh &

![so 5 no 4bb](https://github.com/user-attachments/assets/8652de90-3d03-48d9-bf30-47534e7c37b5)

Command ini berfungsi untuk mengeksekusi file p1.sh di latar belakang sehingga kita tidak harus menunggu hingga selesai untuk bisa menginput command lain

c. ./p1.sh & ./p2.sh & ./p3.sh

![so 5 no 4bbb](https://github.com/user-attachments/assets/8165b65c-dcdd-4fd7-b4d5-798ddc347ffa)
![so 5 no 4bbb1](https://github.com/user-attachments/assets/a575c16a-b511-4c12-99fe-e8e4b6e97c21)

Command ini berfungsi untuk mengeksekusi 3 file tersebut secara bersamaan di latar belakang

d. ( ./p1.sh ; ./p3.sh ) &

![so 5 no 4bbbb](https://github.com/user-attachments/assets/e00255c8-4197-42cf-82e8-8261712da067)
![so 5 no 4bbbb1](https://github.com/user-attachments/assets/ce2295e0-c9c1-49ac-9b77-ba7a5e0efeaf)

Command ini berfungsi untuk mengeksekusi file yang berada di () dulu secara bergantian karena ada ; dan setelah itu di ubah ke latar belakang menggunakan tanda &

# TUGAS-PRAKTIKUM-5-SISTEM-OPERASI

**NAMA : Miki Purnawan**

**NIM : 09011282328122**

**KELAS : SK3B**

**TUGAS PRAKTIKUM 5 SISTEM OPERASI TENTANG JOB CONTROL**

1. Eksekusi seluruh profile yang ada :
   
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

jawab :

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

5. jobs

a.  Buat shell-script yang melakukan loop dengan nama pwaktu.sh,setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  

#!/bin/bash  
while [ true ]  
do  
date >> hasil  
sleep 10  
done  

![so 5 no 5a](https://github.com/user-attachments/assets/831e4396-b269-494c-8f3e-df8cacb9e072)

![so 5 no 5aa](https://github.com/user-attachments/assets/595c45da-8d74-4e08-8243-38683a7bfa93)

Pertama-tama buat file bash dengan nama pwaktu.sh dengan menggunakan nano, kemudian isi file nya sesuai dengan yang di soal, kemudian jika sudah ubah izin akses dari file nya terlebih dahulu agar bisa dieksekusi dengan chmod +x, jika sudah diubah izin akses nya, selanjutnya tinggal jalankan file pwaktu.sh dengan cara ./pwaktu.sh kemudian terminal akan memproses isi file pwaktu.sh, dikarenakan kita menggunakan loop while maka untuk menghentikan nya, kita cukup menekan ctrl + c. Langkah selanjutnya adalah mengecek isi file dari hasil proses eksekusi pwaktu.sh ketika while itu true maka secara otomatis terminal akan megngirimkan output dari tanggal (date) ke file hasil setiap 10 detik, untuk mengecek nya cukup gunakan command cat hasil.

b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut :  
$ jobs  
$ find / -print > files 2>/dev/null &  
$ jobs 

![so 5 no 5b](https://github.com/user-attachments/assets/24086e43-7064-4bf0-91c6-5536e6fe985f)

![so 5 no 5bb](https://github.com/user-attachments/assets/9072857d-22f7-4f9a-9e80-e59b48b604c3)
 
Jalankan program pwaktu.sh ke background dengan menambahkan & setelah ./pwaktu.sh, kemudian ketik jobs untuk melihat program yang sedang berjalan di background setelah itu ketik find / -print > files2>/dev/null command ini berfungsi unntuk mencari semua file dan direktori di sistem mulai dari root (/), menyimpan hasil pencariannya ke dalam file files, membuang semua pesan error, dan menjalankan proses ini di background. lalu ketik jobs lagi untuk melihat daftar proses yang ada di background yang sebelumnya hanya ada proses pwaktu.sh sekarang bertambah menjadi 2 yaitu proses find / -print > files2>/dev/null

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background  
$ fg %1  
$ bg  

![so 5 no 5c](https://github.com/user-attachments/assets/3cec501b-c9e1-45a7-a16b-3012048ea65f)

dari command jobs di bagian b, kita dapat melihat jika ./pwaktu.sh berada di nomor 1 jadi kita akan ubah proses dari pwaktu yang awalnya background menjadi foreground menggunakan command fg %1, lalu untuk menghentikan proses nya sementara, kita tekan tombol ctrl + z maka pwaktu.sh akan berhenti beroperasi baik di bg maupun di fg, dan untuk mengembalikannya kita gunakan command bg dan proses pwaktu.sh akan kembali beroperasi di background

d. Stop program background dengan utilitas kil  
$ ps x  
$ kill [Nomor PID]  

![so 5 no 5d](https://github.com/user-attachments/assets/2102fc21-802b-4e7e-9138-c1a2532ee6d2)

![so 5 no 5dd](https://github.com/user-attachments/assets/1ebb0ebe-08d8-4824-8ba6-582691fd1bd2)

![so 5 no 5ddd](https://github.com/user-attachments/assets/73b778b2-1703-415a-8bc8-d146bf9df9ab)

Pertama-tama gunakan command ps x untuk melihat daftar proses yang sedang berjalan di background beserta nomor PID nya dan karena saya ingin menghapus salah satu proses background dari pwaktu.sh dengan pid 3834 maka kita gunakan command kill 3834 maka proses dari pwaktu.sh dengan nomor PID 3834 akan dihentikan secara permanen, dan untuk melihatnya kita gunakan kembali ps x dan dapat dilihat jika salah satu pwaktu.sh berstatus terminatted.

6. History  

a. Ganti nilai HISTSIZE dari 1000 menjadi 20  
$ HISTSIZE=20  
$ history

![so 5 no 6a](https://github.com/user-attachments/assets/54bde3ff-d3b1-41a8-8897-39fda3b6d9dd)

Ubahlah baris maksimal output yang tersimpan di history menjadi 20 baris dengan menggunakan HISTSIZE=20 setelah itu coba gunakan command history untuk mengecek daftar history nya apakah berubah dari yang awalnya maksimal 10000 menjadi 20 baris saja

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir 
dilakukan  
$ !-5  

![so 5 no 6b](https://github.com/user-attachments/assets/fd789bd4-3a11-4ef7-8beb-9a3e77d211f1)

command !-5 berfungsi untuk menjalankan command dari 5 baris terakhir yang sudah pernah digunakan dan berdasarkan gambar di atas, command HISTSIZE=20 adalah command dari 5 baris terakhir yang sudah pernah digunakan di terminal

c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  
$ !!  

![so 5 no 6c](https://github.com/user-attachments/assets/acefc90d-1e14-4a5b-b94c-e22f29d9d595)

command !! berfungsi untuk menjalankan command terakhir yang sudah digunakan dan ^P dan ^N ini mirip dengan tanda panah atas (untuk ^P) dan tanda panah bawah (untuk ^N) yang fungsinya untuk mencari command yang sudah pernah di gunakan dari yang terakhir kali digunakan sampai command yang pertama kali digunakan jika kalian menekan ^P dalam waktu yang lama sedangkan ^N untuk mengembalikan posisi dari ^P ke command yang paling terakhir digunakan (^ adalah shortcut ctrl pada keyboard)

d.  Ulangi instruksi pada history bufer nomor 150  
$ !150  

![so 5 no 6d](https://github.com/user-attachments/assets/f837c257-1c47-414c-b7e4-9b6a9368046a)

![so 5 no 6dd](https://github.com/user-attachments/assets/f0c205de-df34-4ce9-a970-7eabe642a951)

awalnya saya mencoba command !150 tapi terdapat pesan error, ini dikarenakan dalam history, tidak ada command prompt yang berada di nomor 150 itu karena saya menggunakan device baru untuk mengerjakan tugas praktikum ke 5 dimulai dari soal nomor 4, itulah sebabnya hanya ada 80an total command yang sudah saya gunakan di terminal selama ini dan berhubung di nomor 87 ada command ls -a jadi saya menggunakan !87 untuk memproses command  ls -a yang berada di nomor 87 tanpa harus mengetik command ls -a.

e.  Ulangi instruksi dengan prefix “ls”  
$ !ls 

![so 5 no 6e](https://github.com/user-attachments/assets/c762a2d7-4005-47db-ab81-1117656262c5)

Command ini berfungsi untuk mencari apakah ada command terbaru yang dimulai dengan ls, misalnya ls -l, ls, ls -a dan karena command terbaru yang menggunakan awalan ls ialah ls -a jadi secara otomatis akan memproses command ls -a tersebut. 

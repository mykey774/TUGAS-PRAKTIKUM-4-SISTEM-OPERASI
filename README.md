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

a. PS1=“\! > “ : Command ini untuk mengetahui berapa banyak history command prompt yang sudah kita gunakan dalam terminal dengan menjadikan output dari ! sebagai prompt shell sehingga prompt shell yang awalnya 

b. 


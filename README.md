# Jarkom-Modul-1-IT36-2024

Fico Simhanandi **5027231030**

Agnes Zenobia Griselda Petrina **5027231034**

## Write-Up CTFd Wireshark

## Pegawai Negeri Sebelah (nc 10.15.42.60 53000)
Karena mayoritas protokol menggunakan tcp, maka kita akan filter menggunakan tcp stream eq 1. Lalu kita scrolling untuk menelusuri file yang mengandung isi dari data_pns.csv. Kemudian jawab semua hint berdasarkan file csv.

![Screenshot 2024-09-18 195558](https://github.com/user-attachments/assets/01a6ec8a-a85c-4d08-a0dc-af129393810f)

bisa gunakan fitur find, untuk mencari password yang ditanyakan.

![Screenshot 2024-09-18 195701](https://github.com/user-attachments/assets/6990e7bf-1c00-4ac1-b783-1f3e649f9446)

![Screenshot 2024-09-18 195723](https://github.com/user-attachments/assets/35fb8ddd-6d7c-4059-9269-2169c6bcb9db)

![Screenshot 2024-09-18 195741](https://github.com/user-attachments/assets/d96c2012-1b02-4922-ab32-4e5e24832774)

![Screenshot 2024-09-18 195803](https://github.com/user-attachments/assets/4373d8a4-e087-467f-b8f6-56fa7b6a5bfd)


## EZ (nc 10.15.42.60 54000)
Untuk mencari jawaban dari file.log, kita cari menggunakan tcp.stream eq 0. Lalu saya coba scrolling untuk mencari sesuatu yang suspicious, lalu saya mencoba follow di nomer 638. Kemudian saya menemukan jawaban dari log tersebut. Setelah memasukkan jawaban dari log, saya menemukan portnya yaitu 1234.

![Screenshot 2024-09-18 201052](https://github.com/user-attachments/assets/32513fe6-2e07-43ca-bf64-42ddc42ae291)

![Screenshot 2024-09-18 201201](https://github.com/user-attachments/assets/709fba28-69bf-46bd-915b-e319cb94b4a2)

![Screenshot 2024-09-18 201517](https://github.com/user-attachments/assets/b421cffc-493c-4630-bc3e-dbac4172c621)

![Screenshot 2024-09-18 202841](https://github.com/user-attachments/assets/89fc321c-14b6-4a7c-a792-439b388d8924)


## Corporate Breach (nc 10.15.42.60 51000)
Seperti biasa, kita akan filter menggunakan tcp stream. Saya mencoba-coba untuk follow salah satu nomer dengan protocol HTTP, ada beberapa yang memiliki pesan dari peretas.

![Screenshot 2024-09-18 202853](https://github.com/user-attachments/assets/578575cc-48e7-4356-b8ae-94836f3dcfa2)

Di salah satu file HTTP, saya mencoba no 6. Muncul pesan pengirim bernama Nakhimov.
![Screenshot 2024-09-18 202944](https://github.com/user-attachments/assets/aae7ff68-64d8-4018-aca6-b7d54f254682)

Lanjutkan menjawab semua pertanyaan hint.

![Screenshot 2024-09-18 202952](https://github.com/user-attachments/assets/8b2cc484-0e46-458d-ada0-28c9a7bd0a8c)

Untuk email dan password peretas, saya menyadari bahwa file yang mencurigakan (yang berisi email dan password peretas) memiliki length ysng berbeda dari file yang lain(106). File lain memiliki length sekitar 90an.

![Screenshot 2024-09-18 204102](https://github.com/user-attachments/assets/f4d235d4-abd7-4527-8a34-e45d6b6a1d88)

![Screenshot 2024-09-18 204241](https://github.com/user-attachments/assets/9436bffa-5902-4e49-9fea-b221529cda70)

![Screenshot 2024-09-18 204619](https://github.com/user-attachments/assets/22e346c1-51d0-491b-91dc-048d9cf7ee47)

## Gajah Terbang (Attacker Recon) (nc 10.15.42.60 62000)

Mengikuti soal gajah terbang server, kita akan memfilter untuk mencari file yang berisi semua info user dan product padaa file no 178 (berisi user dan password).

![Screenshot 2024-09-18 231039](https://github.com/user-attachments/assets/8d9d07a3-fb87-4c4c-804f-49edfa323b01)

Lalu kita analisis berdasarkan perubahan yang dilakukan, user kunto aji melakukan perubahan user sehingga user tersebut adalah user peretas.

![Screenshot 2024-09-18 231409](https://github.com/user-attachments/assets/a0ded51f-9ef0-4a54-8c5b-ffe436114d49)

Untuk bagian password, kita dapat melakukan hash pada password kunto aji. 

![Screenshot 2024-09-18 231636](https://github.com/user-attachments/assets/f06c4f6d-b924-4d41-9735-1111252a5975)

Setelah itu kita dapat menjawab seluruh hint sesuai yang kita follow. Seperti yang sebelumnya saya banyak menggunakan fitur coba-coba.

![Screenshot 2024-09-18 231940](https://github.com/user-attachments/assets/7cd6e9ef-ed7b-4e12-ba44-f082d0a1c014)

![Screenshot 2024-09-18 232633](https://github.com/user-attachments/assets/154e9282-52e7-4b5e-bef5-117694001917)

![image](https://github.com/user-attachments/assets/a9674e5e-d87f-496e-b0ab-d85679e55402)


## Advance Sanity Check

Unutk soal ini kita dapat melakukan Follow TCP Stream dan kita menemukan bagian yang cukup menjanjikan dan kita masukan sebagai jawaban

![sanity0](https://github.com/user-attachments/assets/b1aca6e5-7d8f-4358-a47a-0631ed6a7619)


Kita dapat menemukan filename dengan mencari String "file"

![sanity2](https://github.com/user-attachments/assets/24fd5864-6b48-4823-a5bc-cc381ca717c5)


Lalu kita melihat clue yang ada di follow stream tadi yang menyuruh kita ke peraturan soal jarkom dan terdapat tulisan base64 yang didecode menjadi penword dan kita dapat flagnya

![sanity4](https://github.com/user-attachments/assets/414b1472-4314-408f-94ca-5f789f5b4894)


![sanity](https://github.com/user-attachments/assets/139baf24-0498-4ecd-890c-e6ad0d9b5b90)



## Illegal Breakthrough


Untuk kebanyakan jawaban dapat ditemukan di stream ke 1917 atau stream dimana attacker berhasil menembus system

Ip dapat dilihat dengan jelas diawal

![illegal1](https://github.com/user-attachments/assets/f5262838-e1c3-4882-930d-c1330e8dd751)


Kredensial lain dapat dilihat di stream

![illegal2](https://github.com/user-attachments/assets/08e0b16a-051c-4e41-9e84-898f74d6d80f)


Untuk username dan password bisa ditemukan menggunakan ctrl+f dengan search string atau menggunakan stream tadi

![illegal3](https://github.com/user-attachments/assets/89f87194-032c-4330-b82b-f8ca4f07fcb6)



## Package Barrage


Sama halnya seperti Illegal Breakthrough mayoritas jawaban dapat ditemukan lewat stream 1917

Untuk port dapat dilihat di awal

![barrage1](https://github.com/user-attachments/assets/878ba9c5-6f26-43e0-a8b2-fbb8aee1e716)

Untuk bruteforce kita asumsikan bahwa membutuhkan waktu lama untuk hacker menembus sehingga kita langsung melihat stream yang akhir dan menemukan bahwa attacker telah brute force sebanyak 1917 kali

![barrage2](https://github.com/user-attachments/assets/2d01a6e7-754b-41d0-858a-2cff9dee27e8)


Untuk jawaban selanjutnya kita bisa lihat di stream selanjutnya dan scroll kebawah untuk menemukan .txt dan isinya

![barrage3](https://github.com/user-attachments/assets/a042bd50-5bad-46c4-8e04-768d3b3868e3)



## FTP Login


Untuk bagian ini cukup mudah yakni dengan follow TCP stream dan semua jawaban akan muncul di stream ke 4

![ftp1](https://github.com/user-attachments/assets/37b3f90c-1df4-48e2-9387-b3868ae49e62)


![ftp2](https://github.com/user-attachments/assets/3f4e9acb-d2c5-4bb6-9fd5-245791acd82d)



## Surprise


Ini cukup simpel juga yaitu jawaban hampir semua ada di stream yang sama yakni 4, dan untuk jawaban terakhir kita dapat menjalankan code g0tcha.cpp yang diberikan (kita dapat mengambil menggunakan ekstrak maupun langsung copas dari stream 5)

![ftp1](https://github.com/user-attachments/assets/da1525c1-4817-428e-964d-c43df12efd66)


Hasil menjalankan g0tcha.cpp

![surprise](https://github.com/user-attachments/assets/939aaaf5-02cf-4a8d-ab40-89936afa435a)



## Rizzset

Bagian ini untuk domain dapat kita dapatkan dari meng-follow stream UDP dan mendapatkan website its

![rizz1](https://github.com/user-attachments/assets/c802dac0-7c1c-4896-aeac-3487ced83f20)


Ip kita dapatkan dari melihat source/destination

![rizz2](https://github.com/user-attachments/assets/0fe54321-b22e-4c58-ba11-d804b7ffab72)


Untuk bagian ini kita menggunakan bantuan jarm.py yang didownload dari internet

![rizz3](https://github.com/user-attachments/assets/c90d3fc8-b829-4c87-aca7-3a97765a41b2)


Memasukan hasil fingerprint sebagai jawaban

![rizz4](https://github.com/user-attachments/assets/f4672fdd-7f14-471a-96b1-af710c6dacef)



## Gajah Terbang (Server Recon)

Untuk bagian ini, kita dapat melihat kebanyakan dari jawaban di stream TCP ke 9 dan untuk jawaban mengenai PORT dapat dilihat di bagian info

![gajah1](https://github.com/user-attachments/assets/238d03e6-0e16-4e62-9b35-9035fb412211)


![gajah2](https://github.com/user-attachments/assets/657048ed-1ff7-4bcf-9124-2fee2c2f1e12)


Kresendial dari user dan database dapat dilihat dibagian atas stream

![gajah3](https://github.com/user-attachments/assets/0c21c5b7-a001-408d-8ceb-b9857d3d5b48)


![gajah4](https://github.com/user-attachments/assets/bf622543-f56f-441e-b183-36ac30d9e1cc)


Terakhir untuk password kita perlu untuk mendecrypt terlebih dahulu dengan MD5

![gajah5](https://github.com/user-attachments/assets/12e53942-453d-4b84-a482-ff126f4c0c50)



## Malicious code

Untuk Malicious Code kita memakai cara brute force untuk jawaban pertama dan kita menemukan juga stream (54) yang berisi jawaban kedua juga

![malicious1](https://github.com/user-attachments/assets/039c9dde-1657-4f4a-bc1e-44e80c83004a)


Untuk bagian ini kita mengasumsikan bahwa bagian dekat akhir merupakan bagian hacker berhasil masuk ke system dan disini terdapat perhitungan yang salah seharusnya 163 attempt bukan 153

![malicious2](https://github.com/user-attachments/assets/f017a47d-4d31-410f-9a08-d0d05c84bcbe)


Bagian akhir kita mendecrypt kode ASCII yang diberi oleh hacker dan menebak dengan brute force warna-warna yang ada

![malicious3](https://github.com/user-attachments/assets/b11fbc4d-011e-430f-9cae-40f720896232)



## Stegography

Kita dapat melihat terdapat beberapa stream yang memiliki STOR .jpg, sehingga kita dapat menggunakan filter 'frame contains "jpg"' untuk mengambil semua gambar yang ada

![stego1](https://github.com/user-attachments/assets/8a99ae65-e209-4a39-b7af-cb19bf02fac0)


Kita juga menemukan file python di stream yang dimana itu merupakan code yang dapat menekstrak tulisan rahasia dari gambar

![stego2](https://github.com/user-attachments/assets/f787910a-c6ce-460f-80bc-767a58233ca5)


Menggabungkan dan membalik kata-kata tersebut memberikan kita jawaban terakhir

![stego3](https://github.com/user-attachments/assets/79d61ef2-9469-4c3c-9c75-fe9d176d8406)



## 22 Nightmare

Untuk 22 Nightmare terdapat 2 stream yang menarik yaitu stream yang berada di awal dan juga di 141 karena mereka berdua memberikan jpg dan juga .py

![night1](https://github.com/user-attachments/assets/dcd5fbcf-a015-4b36-ac8b-585d00e5af8a)


Saat file didownload maka inilah hasilnya

![night2](https://github.com/user-attachments/assets/b46a1b6a-0f96-4c0b-b3b5-f009d1b3aee5)


![night3](https://github.com/user-attachments/assets/60a4071d-ff53-4b83-a58a-55f48af25be3)


Terdapat hint untuk apa yang harus dilakukan di file.py tadi yaitu berupa XOR decrypt

![night4](https://github.com/user-attachments/assets/10c53702-0124-43cf-be31-8da3e1afac5b)


Terakhir kita melakukan XOR decrypt dengan value angka panjang yang diberikan dan key merupakan hasil BINARY dari tulisan NUN

![night5](https://github.com/user-attachments/assets/8bd5a8d5-30a4-40b1-bd30-f1dd702e62cf)





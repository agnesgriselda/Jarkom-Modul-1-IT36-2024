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

## Gajah Terbang (Attacker RecoN) (nc 10.15.42.60 62000)

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


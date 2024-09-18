# Jarkom-Modul-1-IT36-2024

Fico Simhanandi **5027231030**

Agnes Zenobia Griselda Petrina **5027231034**

### Write-Up CTFd Wireshark

## Pegawai Negeri Sebelah
Karena mayoritas protokol menggunakan tcp, maka kita akan filter menggunakan tcp stream eq 1. Lalu kita telusuri file yang mengandung data_pns.csv. Kemudian jawab semua hint berdasarkan file csv.
![Screenshot 2024-09-18 195558](https://github.com/user-attachments/assets/01a6ec8a-a85c-4d08-a0dc-af129393810f)
![Screenshot 2024-09-18 195701](https://github.com/user-attachments/assets/6990e7bf-1c00-4ac1-b783-1f3e649f9446)
![Screenshot 2024-09-18 195723](https://github.com/user-attachments/assets/35fb8ddd-6d7c-4059-9269-2169c6bcb9db)
![Screenshot 2024-09-18 195741](https://github.com/user-attachments/assets/d96c2012-1b02-4922-ab32-4e5e24832774)
![Screenshot 2024-09-18 195803](https://github.com/user-attachments/assets/4373d8a4-e087-467f-b8f6-56fa7b6a5bfd)

## EZ
Untuk mencari jawaban dari file.log, kita cari menggunakan tcp.stream eq 0. Lalu saya coba scroling untuk mencari sesuatu yang suspicious, lalu saya mencoba follow di nomer 638. Kemudian saya menemukan jawaban dari log tersebut. Setelah memasukkan jawaban dari log, saya menemukan portnya yaitu 1234.
![Screenshot 2024-09-18 201052](https://github.com/user-attachments/assets/32513fe6-2e07-43ca-bf64-42ddc42ae291)
![Screenshot 2024-09-18 201201](https://github.com/user-attachments/assets/709fba28-69bf-46bd-915b-e319cb94b4a2)
![Screenshot 2024-09-18 201517](https://github.com/user-attachments/assets/b421cffc-493c-4630-bc3e-dbac4172c621)
![Screenshot 2024-09-18 202841](https://github.com/user-attachments/assets/89fc321c-14b6-4a7c-a792-439b388d8924)

## Corporate Breach
![Screenshot 2024-09-18 202853](https://github.com/user-attachments/assets/578575cc-48e7-4356-b8ae-94836f3dcfa2)

![Screenshot 2024-09-18 202944](https://github.com/user-attachments/assets/aae7ff68-64d8-4018-aca6-b7d54f254682)
![Screenshot 2024-09-18 202952](https://github.com/user-attachments/assets/8b2cc484-0e46-458d-ada0-28c9a7bd0a8c)
![Screenshot 2024-09-18 204102](https://github.com/user-attachments/assets/f4d235d4-abd7-4527-8a34-e45d6b6a1d88)
![Screenshot 2024-09-18 204241](https://github.com/user-attachments/assets/9436bffa-5902-4e49-9fea-b221529cda70)

![Screenshot 2024-09-18 204619](https://github.com/user-attachments/assets/22e346c1-51d0-491b-91dc-048d9cf7ee47)


# Laporan-Resmi-Jarkom-Modul-1-Kelompok-IT33

Dikerjakan Oleh:
1. Tsaldia Hukma Cita (502723)
2. Ricko Mianto Jaya Saputra (5027231031)

## Advance Sanity Check
Pertama tama, saya mengfilter agar yang hanya http yang ditampilkan, karena jika dilihat sekilah paket dengan http memiliki kata kata yang merujuk pada flag
![Screenshot (205)](https://github.com/user-attachments/assets/ad25248d-1a9f-4a63-bfed-325a9d1e1c5b)
Pada paket dengan info upload.php yang pertama kita dapat menemukan data username dan password
![Screenshot (189)](https://github.com/user-attachments/assets/4dce6f3a-f17b-4e51-8466-08a9b9326948)
Lalu pada paket dengan info upload.php yang kedua kita mendapat data filename beserta extension nya, di paket ini juga terdapat sebuah intruksi untuk diikuti agar menemukan sebuah kode
![Screenshot (190)](https://github.com/user-attachments/assets/c0f7baa4-9852-444f-abec-74fe5abf6287)
Seperti yang telah diintruksikan saya mengecek peraturan soal shift dan mengcopy code yang diselipkan pada halaman ppt tersebut
![Screenshot (202)](https://github.com/user-attachments/assets/2dde50b3-80e0-4334-a9c6-2fe50aa09ebb)
Setelah itu saya mendecode kode yang saya temukan menggunakan decoder online untuk menemukan pesan rahasia yang tersimpan
![Screenshot (192)](https://github.com/user-attachments/assets/3bf26c6c-c966-4bba-804e-4ed908838934)
Setelah semua data terkumpul, saya menginputkan semua data data yang tersedia untuk mendapatkan flagnya
![Screenshot (188)](https://github.com/user-attachments/assets/243c36b6-5ea3-4e44-96bd-2ab1530d1a1d)

## Illegal Breakthrough
Pada soal kali ini saya juga hanya menggunakan filter http saja lalu saya mencari paket dengan info yang cukup berbeda dengan paket yang lain. Disini saya menemukan paket dengan info found, dimana found ini mengindikasikan bahwa attacker telah berhasil untuk login
![Screenshot (197)](https://github.com/user-attachments/assets/f5530dce-1140-4fe1-9432-e0ba369a20b4)
Disini saya membuka paketnya dan menemukan data data yang diperlukan untuk diinputkan (IP, Port, Endpount, Tool, Username, dan Password)
![Screenshot (198)](https://github.com/user-attachments/assets/8f7fa64a-6e16-42e4-9f07-77c1edffc931)
Setelah menemukan data data yang penting, disini saya menginputkan data data tersebut untuk mendapatkan flagnya
![Screenshot (194)](https://github.com/user-attachments/assets/830c924f-82ac-4969-b220-5f0472338411)

## Packets Barrage
Untuk Packets Barrage kurang lebih step awalnya sama dengan Illegal Breakthrough karena soal ini merupakan lanjutan dari soal Illegal Breakthrough
![Screenshot (197)](https://github.com/user-attachments/assets/60153aaf-5a48-4b16-ad9a-7cc923fac8aa)
Untuk paket yang saya buka adalah paket dengan info OK, dimana paket ini terletak dibawah paket yang dibuka pada soal Illegal Breakthrough apabila menggunakan filter http. Dipaket ini terdapat info nama file yang didownload oleh attacker, pesan yang disisipkan oleh attacker
![Screenshot (199)](https://github.com/user-attachments/assets/96e406b4-533f-4a41-836c-2abe3d6ac6d3)
Lalu disini saya mencari banyak attacker melakukan bruteforce menggunakan statistic, lalu http dan paket counter untuk menghitung paket http. Disini juga dapat dilihat terdapat 1916 paket dengan info not found dan 1 paket dengan info found, yang mana hal ini berarti attacker melakukan bruteforce sebanyak 1917 kali
![Screenshot (200)](https://github.com/user-attachments/assets/15ab492a-5b07-4cd4-bc9a-b5f761b3578a)
Lalu setelah data data yang diperlukan terkumpul saya menginputkannya untuk mendapatkan flag dari soal ini. Untuk IP address dari attacker sendiri saya dapatkan setelah mengfilter dimana pada paket found terdapat 2 IP yang mana salah satunya yang berada di kolom dst adalah IP dari attacker
![Screenshot (196)](https://github.com/user-attachments/assets/4a6fa212-0ea9-4ecb-93cb-5d4cff32f9ef)

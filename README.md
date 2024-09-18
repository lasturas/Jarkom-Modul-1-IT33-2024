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


## Pegawai Negeri Sebelah 
Setelah membuka file di wireshark dan melakukan ncat 10.15.42.60 5300. Selanjutnya saya melakukan analisis dan menemukan kejanggalan pada protocol FTP-DATA karena jika dilihat pada bagian info terdapat tulisan data_pns.csv dan terlihat pada bagian pojok kanan bawah bahwa memiliki isi yang panjang. 
![Screenshot (203)](https://github.com/user-attachments/assets/b33a08f3-deda-4c14-8ab0-577a86a105fb)
Setelah di follow terlihat bahwa isinya seperti berikut.
![Screenshot (199)](https://github.com/user-attachments/assets/eb5a8803-a336-49d5-aa21-25697f22a8d9)
Terlihat bahwa data tersebut dapat didapatkan jika melakukan search tcp.stream eq 1. Selanjutnya kita bisa memasukkan data sesuai dengan apa yang diminta pada soal yang tertera di command, seperti Siapa yang memiliki password nNnM%coQuF?, Apa jabatan dari Taufan Kuswandari?, Siapa yang paling awal di list?, Apa password paling akhir dari list? dan akan terlihat bahwa flagnya adalah JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_D4luXbquy8KwwrQuCbH8L6eTYL3MMbXXdujeaB9ViMX0bdbDchWAM4h}
![Screenshot (202)](https://github.com/user-attachments/assets/ca62e770-5a4c-44fb-9ecf-168e780c9af8)

## FTP Login
Setelah membuka file dan melakukan ncat 10.15.42.60 49000, untuk mengerjakannya pertama saya melakukan filter dengan mencari protocol ftp karena soalnya berjudul FTP Login. Setelah melihat soal di cmd ditanyakan bahwa username yang berhasil login maka saya mencari protocol ftp yang memiliki info login succesful dan ketika di follow akan terlihat data seperti berikut ini 
![Screenshot (208)](https://github.com/user-attachments/assets/81da0164-30c9-42de-ad5a-3f240fc41e8b)
Lalu masukkan data yang diminta pada soal di cmd windows seperti user yang berhasil login dan passnya. Setelah itu maka muncul bahwa flagnya adalah JarkomIT{n0t_s0_s3cur3_ftp_qDftQQLou2OXkUMXZbnaJ3R3sL0Dni9cyfxOdGQVMVVLD1DA8ECEG1N}
![Screenshot (211)](https://github.com/user-attachments/assets/ca4fde11-6f76-4a03-b914-894bf6ae9475)

## EZ 
Setelah membuka file dan melakukan ncat 10.15.42.60 54000 saya melihat bahwa pertanyaannya adalah jawaban dari log yang merupakan string. Saya mencoba untuk melakukan follow pada packet pertama dan terlihat isinya seperti berikut ini
![Screenshot (205)](https://github.com/user-attachments/assets/36caa310-3d8a-49b6-a791-d9f1dd56ff00)
Selanjutnya saya isikan data yang ditanyakan: jawabannya jawaban. Selanjutnya untuk mencari port yang digunakan dapat dilihat pada pojok kiri bawah dari packet yang dibuka yaitu 1234 dan terihatlah flag yang dicari yaitu JarkomIT{BiAr_aman_Pake_sSh_teptphneWZQHUWIz7UnNJVHRY3zLleCSvPn7lxHk3RFG8vN8VGgPEZ} 
![Screenshot (207)](https://github.com/user-attachments/assets/95f81061-f4ef-4e63-bd89-306ea77d477b)

## Surprise
Karena file yang digunakan sama dengan FTP Login maka kembali lagi ke file follow yang dibuka tadi, dapat dicari dengan mencari tcp.stream eq 4 dan follow packet pertama. Terlihat isinya seperti berikut ini 
![Screenshot (217)](https://github.com/user-attachments/assets/c80f19f4-d85d-42a2-aa76-d7bbc34417f1)
Untuk service yang digunakan adalah vsFTPd 3.0.3 dapat ditemukan pada bagian atas sendiri. Nama file yang dikirim oleh attacker adalah g0tcha.cpp yang dapat ditemukan pada bagian bawah dengan tulisan STOR g0tcha.cpp. Untuk mencari pesan yang ditinggalkan maka kita bisa mencari packet lain. Saya mulai mencari dari bawah dan menemukan packet protocol FTP-DATA dan isinya seperti berikut ini 
![image](https://github.com/user-attachments/assets/e7b2e69b-2992-4d81-b731-cd2e32d0c889)
Terlihat bahwa pesan tersebut terlihat aneh dan berbeda dari yang lainnya, oleh karena itu saya coba tanya kepada GPT untuk mencari string apa yang tersembunyi pada pesan tersebut dan ternyata isi pesannya adalah g0tchu n0w l1ttl3 m0us3. 
![Screenshot (219)](https://github.com/user-attachments/assets/9cfec46c-65a1-404e-a338-3c2809ac2aaf)
Setelah data dimasukkan maka terlihat bahwa flagnya adalah JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_IhFhAQ8AZNlItqS9L1KYwl81tG0PKAg2feMCzDxlh87tn2cMRiNmTCHU} 
![Screenshot (220)](https://github.com/user-attachments/assets/9226cfc3-8930-46d2-ae8d-fec0449cbc03)

## Corporate Breach
Setelah membuka file dan melakukan ncat 10.15.42.60 51000 saya mencoba melihat isi packet dan menemukan pada packet HTTP berisikan tulisan Hello, my name Nakhimov dan saya coba masukkan data tersebut dan ternyata benar 
![Screenshot (222)](https://github.com/user-attachments/assets/a1e76a73-494d-49f3-8749-0107cbf87290)
Selanjutnya ditanyakan email untuk login saya merasa bahwa informasi tersebut bisa ditemukan pada protocol HTTP lainnya, oleh karena itu saya search HTTP dan melihat di bagian bawah terdapat packet yang aneh dengan info OK yang berbeda dari yang lain tanpa adanya (text/html) dan terlihat bahwa isi data terdapat email dan saya coba masukkan dan benar.
![Screenshot (223)](https://github.com/user-attachments/assets/614dcd37-5653-4b9b-a0da-73d5b73de799)
Emailnya adalah jarkomsupport@gmail.com dan passnya adalah j4rk0mg4c0rbg dan terlihat bahwa flagnya adalah JarkomIT{supp0rt_k0k_l3m4h_bg_148t3OczwFaXR6XeeNzSmOC1UG6aNJhRSEPFc6MTufWLndDfW2qwG6}

## Rizzset
Setelah membuka filenya dan melakukan ncat 10.15.42.60 59500, ditanya domain apa yang di dns. Oleh karena itu saya search DNS protocol 
![image](https://github.com/user-attachments/assets/8a80c6a2-f249-49a7-a2cf-620f7f6ac053)
Pada gambar tersebut terlihat bahwa pada info packet pertama terdapat info tulisan www.its.ac.id dan saya coba masukkan dan benar ternyata. Selanjutnya ditanyakan untuk IPnya dapat ditemukan pada no8 yang ada di gambar pada bagian info yaitu 103.94.189.5.
Selanjutnya ditanyakan untuk pesan JARM. Pada bagian ini saya sempat stuck dan tidak paham dengan apa yang dimaksud, awalnya saya kira untuk pesan yang dicari dapat didapatkan dari salah satu packet, ternyata setelah mencari di google ternyata harus melakukan beberapa step untuk mendapatkan pesan JARM yang dimaksud. Pertamanya melakukan clone github, lalu masuk kedalam vscode dan pindah menuju folder jarm, lalu masukkan command python jarm.py -v www.its.ac.id (domain yang didapat tadi) tunggu hingga muncul pesan JARM: 2ad2ad16d2ad2ad22c2ad2ad2ad2ad74aaecca9f9c4a3303863dfee62b241e seperti gambar di bawah ini 
![Screenshot (225)](https://github.com/user-attachments/assets/77d2fe0e-0285-4fb4-821d-f907e7d91ff5)
Dan ditemukan bahwa flagnya adalah JarkomIT{Dn5_C0rR34t10n_uFpIMbIlWzkmThg1WPhmE0lqLr1zZzSa247oTXSAIiysJ1WRGOT2bU1T5}

## Gajah Terbang (Server Recon)
Setelah membuka file dan melakukan ncat 10.15.42.60 61000 saya mencoba melihat beberapa packet dan saya menemukan bahwa packet TCP ada banyak dan terlihat mencurigakan, oleh karena itu saya search protocol TCP dan menemukan hal aneh pada salah satu packet TCP, yaitu ia memiliki panjang yang lebih panjang dibanding packet yang lain dan isinya terdapat email-email. Ketika dilakukan follow maka terlihat isinya seperti berikut ini 
![image](https://github.com/user-attachments/assets/e02b6ef3-7cee-4159-9507-1ce4ccefe5ce)
Karena pertanyaan pertama adalah DBMS apa yang digunakan saya bingung akan artinya, tetapi saya sedikit curiga dengan pgsql karena pada format jawaban tertulis software seperti MonggoDB. Namun, ketika saya masukkan pgsql ternyata jawaban salah, lalu saya mencoba untuk memastikan apa tu pgsql di google dan terlihat bahwa itu merupakan singkatan dari PostgreSQL dan ketika saya masukkan ternyata benar. Soal selanjutnya adalah pada port berapa server tersebut berjalan. Karena pada soal sebelumnya juga sudah ditanyakan port maka saya mencoba untuk mencari pada letak yang sama yaitu pada pojok kiri bawah pada packet yang saya buka dan saya mencoba memasukkan port yang ada di bawah tersebut. Ternyata port yang benar adalah port 6969.
Selanjutnya untuk OSnya adalah Debian. Selanjutnya ditanyakan user serta nama database dapat ditemukan pada bagian atas packet yang sudah di follow. Untuk jumlah user dapat didapatkan dengan menghitung jumlah email yang tertera, yaitu 4. Selanjutnya ditanyakan email dan pass admin, dapat ditemukan pada email jojohermawan@gmail.com karena jika dilihat pada bagian role jojo merupakan admin. Namun, untuk passnya bisa didapatkan dengan melakukan decode c93ccd78b2076528346216b3b2f701e6 menjadi admin1234 dengan MD5 pada web online seperti gamber di bawah. 
![Screenshot (227)](https://github.com/user-attachments/assets/d599a46e-5559-4b90-8ef3-09384a937681)
Lalu muncul flag yang dicari yaitu JarkomIT{Gy4tT_M5g_4U_i8AIpkyO6erhKPj9xCMTlwjyh5k1aiwKMR1kjk7nbt7UH2phtFksTBiD1}
![Screenshot (228)](https://github.com/user-attachments/assets/37eb4313-365b-4254-84d9-3291de6d6ee3)

## Gajah Terbang (Attacker Recon)
Karena filenya sama maka kita bisa langsung melakukan ncat 10.15.42.60 62000 dan ditanyakan akun email yang digunakan penyerang. Karena di data packet yang sama terdapat 4 email, maka saya mencoba untuk menganalisa email tersebut dan saya menemukan pada role terdapat email yang mencurigakan. Email kuntoajiisrillll@gmail.com terlihat mencurigakan karena pada role dia merupakan userC yang berbeda dengan yang lain, yang lain memiliki role userD. Setelah dimasukkan ternyata benar, dan pertanyaan selanjutnya adalah pass dari si aji ini. Untuk mendapatkan passnya kita bisa melakukan hal yang sama seperti saat kita mencari pass dari admin, yaitu decode aa1cbddbb1667f7227bcfdb25772f85c menjadi kissme menggunakan MD5. Untuk tanggal adalah 2024-06-09 yang dapat ditemukan pada bagian banned user. Untuk yang diubah adalah users dan banned_users karena saya coba-coba memasukkan dan ternyata benar. Untuk barang yang dibeli juga saya coba memasukkan pilihan yang ada, dan ternyata yang benar adalah rokok dan es krim. Untuk total belanjaan tinggal menambahkan saja harga rokok 18.000 dan es krim 6.500, jadi totalnya adalah 24.500 dan muncul flagnya adalah JarkomIT{G4jaH_K0k_t3RbaNG_55nGARkEFvELFXSfNP6QXxCmjYntjdYJhpjmOu8ELGy26MGvuyx2QKt5}
![Screenshot (229)](https://github.com/user-attachments/assets/7b138402-6b87-4cd4-bed2-ba5397aaabc0)
![Screenshot (230)](https://github.com/user-attachments/assets/90e1c2ec-fbda-4a7e-a6a0-da2f35b536f2)


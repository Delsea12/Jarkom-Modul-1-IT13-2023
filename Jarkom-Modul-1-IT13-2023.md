# Jarkom-Modul-1-IT13-2023

|       Nama      | NRP        | 
| -----------     | :---------: 
| Della Setyowati | 5027211044 | 
| Wisnu Adjie Saka| 5027211051 | 

#### 1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
##### a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
##### b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
##### c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
##### d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

- 

#### 2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
- Karena yang ditanyakan web server, yang pertama kita lakukan adalah filtering dengan kata "HTTP"
- Setelah itu follow HTTP streamnya
- Langsung muncul nama server yang digunakan pada HTTP stream tersebut

![Screenshot 2023-09-21 224338](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/edc1c4cc-14fe-4395-9e3b-cff30e4e78eb)

![Screenshot 2023-09-21 224354](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/ae6a3b4f-2559-4507-8ff1-51050e2100e8)

![Screenshot 2023-09-21 224408](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/e4d5f44c-0e59-41b2-add1-2437122212cd)

#### 3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
##### a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702 
##### b. Protokol layer transport apa yang digunakan?

- Yang pertama kita harus melakukan filtering dengan query  “(ip.dst == 239.255.255.250) && udp.port == 3702” , jadi nanti akan terfilter IP destination 239.255.255.250 dengan port 3702
- Setelah itu untuk mengetahui berapa banyak paket yang berjalan bisa di cek di kanan bawah , yaitu 21 paket
- Dan protocol yang yang digunakan juga bisa di cek di section protokol, yaitu UDP

![Screenshot 2023-09-21 225300](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/a7908c19-bb5e-42a4-86a5-fe955ab5356f)

![Screenshot 2023-09-21 225318](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/692128c2-2daf-4f7a-812f-a9429ca6542b)

#### 4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?
- Pada no 4 kita diminta untuk mencari nilai checksum dari pada paket nomor 130, kita bisa mencari yang paket nomor 130
- Mencari nilai checksum dan ditemukan pada header dalam User Datagram Protocol

![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154384396749651990/image.png)

- Membaca flag bisa melalui ubuntu dengan melakukan nc 10.21.78.111 13591 maka akan didapatkan flags Jarkom2023{ch3cksum_is_u5eful_0x9e8u}. Dengan memasukan 0x18e5 yang terdapat pada checksum 
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154384442194931793/image.png)

#### 5. Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
##### a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
##### b. Port berapakah pada server yang digunakan untuk service SMTP?
##### c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

- Jadi pada soal ini diberikan 2 file, file pcap dan file zip, pada soal ini berbeda dari yang lain, nc nya tidak diberikan
- Pada saat file zip nya dibuka terdapat sebuat file .txt yang diberikan password
- Untuk mencari clue untuk pw nya kita bisa membuka file pcap nya, dan cek-cek stream TCP nya
- Setelah melakukan investigasi, telah ditemukan clue untuk pw nya yaitu encode dari password nya menggunakan Base64
- Kita langsung melakukan decode Base64 , langsung didapatkan nya password untuk membuka file .txt tersebut, yang ternyata berisi nc dari soal ini, akhir nya kita bisa menjawab soal dari nomor ini
- Kita dapat melihat jumlah paket di file tersebut pada kanan bawah, ada 60 paket
- Lalu kita bisa melakukan filtering dengan kata kunci SMTP untuk mencari letak protocol itu ada di port berapa, dia ada di port 25
- Dan akhirnya untuk mengetahui mana IP yang publik, kalian bisa mencoba semua IP yang ada di file tersebut sampai benar, karena di file tersebut hanya terdapat 2 IP jadi gunakan cara ini saja ( IP yang publik “74.53.140.153”)

![Screenshot 2023-09-21 230521](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/780630a7-a7d8-4279-99fe-330f3b15928d)

![Screenshot 2023-09-21 230536](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/0363b81e-7807-4dc1-86b8-675007c24dad)

![Screenshot 2023-09-21 230549](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/675820e2-f52f-4248-a562-3cb947ec4ba6)

![Screenshot 2023-09-21 230603](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/80edb669-a5cc-408c-942b-3c6e425e083e)

![Screenshot 2023-09-21 230618](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/c6d5839d-6f59-4472-b355-35e7b5b861c7)

![Screenshot 2023-09-21 230633](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/d24078d9-2a04-40b9-9a3b-7615553e2400)

![Screenshot 2023-09-21 230645](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/7a7a3508-3878-4567-94ce-167855480bc2)

#### 7. Berapa jumlah packet yang menuju IP 184.87.193.88?
- Mendapatkan jumlah packet ip 184.87.193.88 bisa dilakukan dengan cara memfilter ip address tersebut pada display filter, selanjutnya kita dapat mengetahui jumlah dari ip packet tersebut, dan didapatkan sebanyak 6
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154390030589112451/image.png)
- Kemudia membaca dan mengetahui flagsnya bisa dilakukan melalui ubuntu dengan cara nc 10.21.78.111.6565 dan didapatkan flags bisa dilihat pada gambar dibawah
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154390091058389002/image.png)

#### 8. Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad).

- Disini kita hanya diminta untuk memasukan query untuk menuju port 80, dan kita bisa menggunakan udp.dstport == 80 || tcp.dstport == 80nc 10.21.78.111 7171
- ```tcp``` dan ```udp``` merupakan protokol, ```dstport``` merupakan filter yang kita cari untuk menampilkan paket yang menuju port 80. Dan kita bisa melakukan membaca flag menggunakan nc ```nc 10.21.78.111 7171``` maka akan didaptkan flags seperti dibawah ![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154391829802922014/image.png)

#### 9. Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
- Disini dapat langsung dilakukan memfilter query dengan menggunakan ip.src == 10.51.40.1 && ip.dst != 10.39.55.34. Dimana kita hanya bisa mengambil alamat dari 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34
- Untuk mendapatkan flags dan memfilter query dapat langsung dilakukan pada ubuntu 

![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154393256273125376/image.png)

#### 10. Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
- Pertama kita melakukan filtering dengan kata kunci "Telnet"
- Lalu kita follow TCP stream nya (boleh yang mana saja yg penting protocol telnet)
- Setelah follow stream nya, akan ada kredensial id dan password
- Untuk mendapatkan kredensial yang benar, bisa di cek satu per satu setiap kredesnsial pada stream nya untuk di input di nc yang sudah disediakan pada soalnya
- Setelah mendapatkan kredensial yang benar , akan langsung dapat flag nya

![Screenshot 2023-09-21 223838](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/f0971ebb-7eb0-4064-b77c-630773ffae0e)

![Screenshot 2023-09-21 224202](https://github.com/Delsea12/Jarkom-Modul-1-IT13-2023/assets/113821220/a4a071ff-ea27-4542-9e50-b03cfccd80af)


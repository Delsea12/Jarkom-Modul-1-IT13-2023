# Jarkom-Modul-1-IT13-2023

|       Nama      | NRP        | 
| -----------     | :---------: 
| Della Setyowati | 5027211044 | 
| Wisnu Adjie Saka| 5027211051 | 

#### 4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?
- Pada no 4 kita diminta untuk mencari nilai checksum dari pada paket nomor 130, kita bisa mencari yang paket nomor 130
- Mencari nilai checksum dan ditemukan pada header dalam User Datagram Protocol

![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154384396749651990/image.png)

- Membaca flag bisa melalui ubuntu dengan melakukan nc 10.21.78.111 13591 maka akan didapatkan flags Jarkom2023{ch3cksum_is_u5eful_0x9e8u}. Dengan memasukan 0x18e5 yang terdapat pada checksum 
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1154384442194931793/image.png)

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

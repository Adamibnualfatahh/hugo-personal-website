---
title: "Install CI3"
date: 2021-10-06T14:48:16+07:00
theme: "PaperMod"
author: Adam Ibnu
comments: true 
ShowBreadCrumbs: true
ShowReadingTime: true
ShowToc: true
---

## Pengenalan
Codeigniter merupakan sebuah framework php yang sangat sederhana, ringan, dan mudah untuk dipelajari, codeigniter sendiri telah mengadopsi pola `MVC` yaitu Model-View-Controller dimana kita dapat memisahkan logika dan tampilan sebuah website yang ingin dibangun dengan framework berbasis MVC ini.

Namun yang perlu diperhatikan dalam tahap dasar ini sebelum kita memulai seharusnya kita telah mengerti konsep `OOP (Object Oriented Programming)` agar lebih mudah memahami cara kerja sebuah framework.

## Installasi Framework

> ### 1: Download file Codeigniter

Kalian bisa download pada halaman resmi CodeIgniter https://codeigniter.com/download. Pilih CI versi 3 

> ### 2: Ekstrak dan Install Codeigniter Framework

Setelah kalian download maka kalian akan mendapatkan file bernama CodeIgniter-3.1.3.zip.
Lalu silahkan ekstrak file dan rename sesuai dengan nama project yang kalian akan buat.
Setelah itu kalian letakkan folder ke dalam directori Xampp/htdocs/

> ### 3: Konfigurasi Base URL

Setelah kalian masukan file kedalam htdocs sekarang kalian buka text editor kalian dan buka file tadi kedalam text editor kesayangan kalian.
Selanjutnya kalian buka bagian application/config/config.php cari kode 
```php
$config['base_url'] = '';
```
dan ubahlah menjadi 
```php 
$config['base_url'] = 'http://localhost/namafile';
```

Nilai tersebut harus sesuai dengan alamat/nama folder yang kalian tentukan ketika anda menyalin file codeigniter ke dalam folder root web server kalian

> ### 4: Selesai

Setelah semua sudah dilakukan sesuai dengan instruksi diatas silahkan buka browser dan ketikan url `http://localhost/namafile`, jika berhasil akan keluar tampilan seperti gambar dibawah ini:
![CI3](/img/welcome.jpeg)


---
title: "Membuat CSS di dalam HTML"
date: 2021-08-21T05:48:22+07:00
draft: false
author: Adam Ibnu
comments: true 
ShowBreadCrumbs: true
ShowReadingTime: true
ShowToc: true
---

>*source :
[Kopiding](https://kopiding.in/)*

## Pemanasan 
Tampilan atau interface memiliki peran penting dalam suatu aplikasi tak terkecuali aplikasi berupa website. Hal ini karena tampilan merupakan salah satu faktor bagaimana suatu website bisa menarik para pengunjung.

Dengan adanya tampilan yang cantik maka pengunjung akan betah berlama-lama di website kita. Semakin cantik tampilan website maka pengunjung akan semakin tertarik menelusuri berbagai konten yang ada dalam website kita.

Untuk mengatur tampilan website dalam HTML perlu adanya kerjasama dengan yang namanya CSS.

## Mengenal CSS
CSS merupakan singkatan dari Cascading Style Sheet yang fungsi utamanya yaitu mengatur tampilan dari elemen yang ditulis pada dokumen HTML. Bahasa inilah yang memiliki peran penting untuk mempercantik tampilan antarmuka (interface) website

 >## Menambahkan CSS ke Dokumen HTML

## Inline CSS
Inline CSS adalah cara menambahkan CSS dengan menggunakan atribut style pada tag pembuka elemen HTML. Cara ini biasanya digunakan untuk memberi gaya atau style unik pada suatu elemen.

```HTML
<!DOCTYPE html>
<html>
<head>
	<title>Mengenal CSS</title>
</head>
<body>
	<h1 style="padding: 5px; background-color: red;">Tutorial Penerapan CSS</h1>
	<p style="padding: 10px; background-color: green;">
		Selamat datang di website kami!
	</p>
</body>
</html>
```
Hasil:
![](https://ik.imagekit.io/bq0dkmk6a/wp-content/uploads/html-css-2.png)

## Internal CSS
Internal CSS merupakan cara menambahkan CSS dengan menggunakan tag `<style>` di dalam tag `<head>`. Cara ini diperuntukkan untuk mengatur style untuk satu halaman website.
```
<!DOCTYPE html>
<html>
<head>
	<title>Mengenal CSS</title>
	<style type="text/css">
		h1{
			padding: 5px; 
			background-color: red;
		}
		p{
			padding: 10px; 
			background-color: green;
		}
	</style>
</head>
<body>
	<h1>Tutorial Penerapan CSS</h1>
	<p>Selamat datang di website kami!</p>
</body>
</html>
```
Hasil:
![](https://ik.imagekit.io/bq0dkmk6a/wp-content/uploads/html-css-2.png)

## Eksternal CSS
Eksternal CSS adalah cara menambahkan CSS dengan menggunakan tag `<link>` yang didefinisikan pada setiap dokumen HTML. Cara ini merupakan cara yang paling umum digunakan oleh para pengembang, karena dengan cara ini memungkinkan kita untuk membuat hanya satu style CSS yang kemudian dapat diterapkan ke semua halaman website.

Untuk menerapkan cara ini kita perlu menulis kode CSS secara terpisah dari dokumen HTML.

Kemudian dokumen HTML dan file dari kode CSS tadi selanjutnya dihubungkan dengan menggunakan tag `<link>` yang didefinisikan pada bagian `<head>` dalam dokumen HTML.

Untuk lebih jelasnya perhatikan contoh penerapan berikut:

Buat file index.html dengan isi sebagai berikut:
```
<!DOCTYPE html>
<html>
<head>
	<title>Mengenal CSS</title>
</head>
<body>
	<h1>Tutorial Penerapan CSS</h1>
	<p>Selamat datang di website kami!</p>
</body>
</html>

```
Kemudian tambahkan tag `<link>` di dalam tag `<head>`
```
<link rel="stylesheet" type="text/css" href="style.css">
```
Buat file kembali dengan nama style.css dan tulis kode CSS di bawah ini:
```
h1{
	background-color: red;
	padding: 5px;
}
p{
	background-color: green;
	padding: 10px;
}
```

Hasil:
![](https://ik.imagekit.io/bq0dkmk6a/wp-content/uploads/html-css-2.png)


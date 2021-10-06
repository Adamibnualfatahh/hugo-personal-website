---
title: "CREATE HTML IN PHP "
date: 2021-08-23T11:16:57+07:00
draft: false
comments: true 
author: ["Adam Ibnu", "PHP"]
ShowBreadCrumbs: true
ShowReadingTime: true
ShowToc: true
---

## Membuat HTML di dalam PHP

>Belajar untuk mengajar

## PHP Dan HTML 
PHP dan HTML banyak berinteraksi: PHP dapat menghasilkan HTML, dan HTML dapat menyampaikan informasi ke PHP.
 
>Encoding/decoding

Encoding/decoding apa yang saya perlukan ketika saya memberikan nilai melalui formulir/URL?
Ada beberapa tahap yang pengkodeannya penting. Dengan asumsi Anda memiliki string $data, yang berisi string yang ingin Anda teruskan dengan cara yang tidak disandikan, ini adalah tahapan yang relevan:
>interpretasi HTML.

interpretasi HTML. Untuk menentukan string acak, Anda harus memasukkannya dalam tanda kutip ganda, dan htmlspecialchars() seluruh nilai.
>URL

URL: Sebuah URL terdiri dari beberapa bagian. Jika Anda ingin data Anda ditafsirkan sebagai satu item, Anda harus menyandikannya dengan urlencode().

## Contoh 1
```
<?php
    echo '<input type="hidden" value="' . htmlspecialchars($data) . '" />'."\n";
?>
```
>Note: It is wrong to urlencode() $data, because it's the browsers responsibility to urlencode() the data. All popular browsers do that correctly. Note that this will happen regardless of the method (i.e., GET or POST). You'll only notice this in case of GET request though, because POST requests are usually hidden.

## Contoh 2
```
<?php
    echo "<textarea name='mydata'>\n";
    echo htmlspecialchars($data)."\n";
    echo "</textarea>";
?>
```
>Note: The data is shown in the browser as intended, because the browser will interpret the HTML escaped symbols. Upon submitting, either via GET or POST, the data will be urlencoded by the browser for transferring, and directly urldecoded by PHP. So in the end, you don't need to do any urlencoding/urldecoding yourself, everything is handled automagically.

## Contoh 3

```
<?php
    echo '<a href="' . htmlspecialchars("/nextpage.php?stage=23&data=" .
        urlencode($data)) . '">'."\n";
?>
```
>Note: In fact you are faking a HTML GET request, therefore it's necessary to manually urlencode() the data.


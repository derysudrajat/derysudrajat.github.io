---
title: Custom Shape ImageView menggunakan CardView Android
tags: [Android, Technology]
style: 
color: 
description: Hai guys hari ini aku mau nge-share tutorial membuat custom shape pada Image View menggunakan Card View, beberapa waktu lalu teman kampusku ada yang menanyakan sesuatu ke aku pribadi “Gimana sih cara ngubah ImageView agar bentuknya lingkaran?”
---

Source: [Dery Sudrajat](https://medium.com/@dery.io/custom-shape-imageview-menggunakan-cardview-android-4bba93884bf9)

{% include elements/figure.html image="https://miro.medium.com/max/1400/0*PgXjLIXlSwz6-E4R.png"%}

Hai guys hari ini aku mau nge-share tutorial membuat custom shape pada Image View menggunakan Card View, beberapa waktu lalu teman kampusku ada yang menanyakan sesuatu ke aku pribadi

> **“Gimana sih cara ngubah ImageView agar bentuknya lingkaran?”**

Pada dasarnya sebuah ImageView pada Android tidak memiliki **corner_radius** pada atribut aslinya, jika kita ingin membuat ImageView kita memiliki bentuk lingkaran kita bisa menggunakan library pihak ketiga contohnya library dari **[de.hdodenhof:circleimageview](https://github.com/hdodenhof/CircleImageView)** atau kalian bisa cek langsung di laman githubnya.

{% include elements/figure.html image="https://miro.medium.com/max/1080/0*jtJgDFC_epRKtghe" caption="Circle ImageView menggunakan library dari de.hdodenhof:circleimageview" %}

Library tersebut memang bisa mengubah imageview kebentuk lingkaran tetapi tidak bisa membuat bentuk yang hanya memiliki sebagian corner radius. Lalu gimana cara membuat ImageView yang lebih costum atau kita sesuaikan sendiri?

Oke oke tenang, masalah ini kita bisa selesaikan dengan menggunakan CardView, CardView pada dasarnya memiliki atribut corner_radius, yang kita bisa gunakan sebagai bahan dalam memecahkan masalah ini. Oke kita langsung aja ke CodeLab.

### CodeLabs

{%- gist db9d168ade77ca7ea97a2b800f4f4742 %}

Pada kode diatas kita memiliki CardView dengan ukuran 100dp x 100dp, dimana kita bisa menambahkan **app:cardCornerRadius=”16dp”** yang akan membuat lengkung pada sisi CardView dengan lebar 16dp. Setelah itu kita bisa menambahkan ImageView sebagai Child dari CardView seperti pada kode ditas, kita hanya perlu menggunakan **match_parent** pada lebar dan tinggi dari ImageView agar mengikuti lebar dari CardView dan selesai kamu bisa membuat ImageView dengan lengkung pada sisinya, kamu bisa mengganti lebar lengkung dari CardView (**app:cardCornerRadius**) untuk membuat ImageView dengan lengkung yang berbeda.

{% include elements/figure.html image="https://miro.medium.com/max/668/1*MMVae_CfqTauEHseEt7xSg.png" caption="Contoh hasil implementasi Custom ImageView menggunakan CardView" %}

Lalu bagiamana membuat ImageView yang bentuknya lingkaran menggunakan CardView?, hal ini cukup mudah kita hanya perlu mengatur **app:cardCornerRadius** pada CardView menjadi **setengah** dari **lebar** dan **tinggi** dari CardView, contohnya pada kode di atas kita mengatur lebar dan tinggi Card adalah **100dp**, untuk itu jika kita ingin membuat bentuk ImageView lingkaran kita harus mengatur **app:cardCornerRadius** setengah dari itu yaitu **50dp**. Cukup mudah kan, selamat kamu sudah membuat **Custom ImageView** menggunakan **CardView**.
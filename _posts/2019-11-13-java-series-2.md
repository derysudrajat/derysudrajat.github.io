---
title: Program Pertama | Java Series 2
tags: [Java, Technology]
style: fill
color: light
description: Oke ges hari ini kita mau bahas tentang Java Basic, apa aja sih yuk kita bahas disini, jadi di tulisan kemarin kan kita sudah membahas cara untuk instalasi IDE untuk series ini.
---

Source [Dery Sudrajat](https://medium.com/@dery.io/program-pertama-java-series-2-a22e5f8d23a7)

Hello ges, apa kabar semuanya…. aku harap kalian dalam keadaan wadidaw luar biasa. Sebelum mulai aku minta maap nih udah lama banget ga nulis wkwk, karena kesibukan organisasi dan kuliah yang super cape begadang terus ges, jangan ditiru ya, tapi sekarang aku udah mulai selesai semua jadi bisa nulis lagi deh, wkwkw malah curhat kan wkwkw. Oke ges hari ini kita mau bahas tentang Java Basic, apa aja sih yuk kita bahas disini, jadi di tulisan kemarin kan kita sudah membahas cara untuk instalasi IDE untuk series ini, buat kalian yang belum baca bisa ke link berikut [Tools-Java Series #1](https://derysudrajat.github.io/blog/java-series-1), kalau sudah oke kita bisa lanjut yaa —

#### Membuat Proyek Pertama
Oke sekarang kita akan membuat program pertama di java, pertama-tama kalian buka Intellij IDEA nya dulu ya. jika sudah nanti tampilannya akan seperti ini, selanjutnya apa?..

1. Kita klik Create New Project {% include elements/figure.html image="https://miro.medium.com/max/956/1*0oqcbA8h-YWzPzxd0wN5-A.png"%}
2. Setelah itu akan muncul seperti ini. setelah itu atur SDK untuk project ini sesuaikan dengan SDK kalian ya, setelah itu klik **NEXT**. {% include elements/figure.html image="https://miro.medium.com/max/1400/1*KxTXzSWPWjPpV72J9d1Kcg.png"%}
3. Nanti ketika muncul seperti ini klik **NEXT** saja. {% include elements/figure.html image="https://miro.medium.com/max/1400/1*Cx6s_R8hed9jmyhfU0HxTg.png"%}
4. Setelah itu kita beri nama proyek kita dengan nama “ProgramPertama”. klik **FINISH**. {% include elements/figure.html image="https://miro.medium.com/max/1400/1*8o6Z8S8gnow7iV-ai7tzqA.png"%}

Jika sudah selesai tampilan IDE akan seperti ini.

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*ueTdwqqLTdJT_0mXTixRZQ.png"%}

#### Membuat Kelas Baru
setelah kita membuat proyek baru kita akan menambahkan sebuah kelas baru pada proyek kita untuk bisa dijalankan nantinya, yuk lanjut.

Setelah itu kita buat Java Class baru degan klik folder src-new-Java Class

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*fgTjgNtc65CnEjW-Pfmvvw.png"%}

Setelah itu kita beri nama kelas baru tersebut dengan nama **“main”**, lalu pilih yang Class atau tekan **Enter**.

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*4snLPLjKsmjwsMPT0MIN_g.png"%}

Setelah kelas dibuat tambahkan kode berikut pada kelas tersebut, usahakan diketik sendiri ya jangan di copy-paste, karena pengalaman programming adalah dengan menuliskan kode sendiri ingat…

{%- gist 6d21b6ec90c709935f07e2100cfa40c5 %}

nah disini ada sedikit trik nih buat nilis kode lebih simple, ketika kalian ingin membuat method void main kalian ga perlu nulis semua ges cukup ketik **“main”** seperti contoh berikut. setelah itu klik **“ctrl+space”** nanti akan mucul sebuah suggestion untuk kode yang kita tulis tadi. Setelah itu tinggal tekan **Enter**.

{% include elements/figure.html image="https://miro.medium.com/max/1116/1*VMQB4D8LTXSdvA3wZE2R_g.png"%}

Setelah method main terbuat, lahkah selanjutnya membuat output yang akan kita cetak di termial caranya gimana?, sama saja di sini ada trik untuk tidak menulis kode yang panjang System.out.println(), ini akan memakan waktu, apa triknya? cukup tulis **“sout”** nanti akan mucul seperti pada gambar dibawah ini, dan tekan **Enter**, dan selesai wadidaw gampang banget kan, ga perlu nulis panjang-panjang, karena itulah fungsi IDE, mepermudah para programmer untuk membuat program.

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*HpJgOMs2WczNjUXdRdrzfQ.png"%}

#### Menjalankan Kelas main
Setelah kita menuliskan kode diatas kita akan menjalankan kode tersebut coba perhatikan gambar di bawah.

{% include elements/figure.html image="https://miro.medium.com/max/848/1*x5PaJ3ko4Q1tWKI9RhYQYA.png"%}

untuk menjalankan kode kita cukup klik tombol play berwarna hijau untuk menjalankan kode yang kita buat. Maka hasilnya akan seperti di bawah ini.

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*8rj7kgt7vR1cB_brTen24A.png"%}

Oke mungkin postingan kali ini sekian dulu, nanti kita akan lanjut minggu depan dengan melanjutkan ke materi dasar dasar dari Java itu seperti apa, oke ges makasih udah baca dan sampe juma minggu depan, dan seperti biasa salam **#ubahdengankode**.
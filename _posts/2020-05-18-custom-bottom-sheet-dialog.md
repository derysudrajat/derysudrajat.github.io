---
title: Create an Android Custom Bottom Sheet Dialog with RecycleView
tags: [Android, Technology]
style: fill
color: danger
description: Hari ini aku mau share tentang apa yang aku baru belajar kemarin yaitu mau bikin dialog yang bisa muncul dari bawah gitu loh, nah itu namaya Bottom Sheet Dialog
---

Source: [Dery Sudrajat](https://medium.com/@dery.io/create-an-android-custom-bottom-sheet-dialog-with-recycleview-6452ef61cf1)

{% include elements/figure.html image="https://miro.medium.com/max/2000/1*P2SF84Md4xQK7_f6JiOEcw.png"%}

Haloo semuanya, udah lama banget ga posting nih hehe, mumpung sekarang lagi senggang karena liburan lebaran jadi mau rajin nulis lagi nih. Gimana kabar kalian? semoga semuanya baik-baik aja ya, lagi masa pandmi ini kita memang harus terus jaga kesehatan, kalau aku sih biasanya banyak minum vitamin c dan cukup tidur, sama sering cuci tangan aja. Masa seperti ini bukan berati kita harus stop buat berkreasi, jadi harus tetep produktif dan selalu memberikan manfaat untuk yang orang lain dalam bentuk dan kemampuan yang kita bisa.

Oke udah ya curhatnya hehe, jadi hari ini aku mau share tentang apa yang aku baru belajar kemarin yaitu mau bikin dialog yang bisa muncul dari bawah gitu loh, nah itu namaya **Bottom Sheet Dialog**. Jadi kemarin ceritanya lagi bikin proyek android kan ya, nah kebetulan proyeknya butuh komponen seperti itu, sementara aku juga belum tau nih, jadi coba cari-cari di dokumentasi google material dan lainnya, akhirnya nemu dan mau coba aku share lagi di sini.

Jadi apa itu Bottom Sheet Dialog? Simplenya kalian kalau mau share barang di toko online ke temen kalian buat minta traktir beliin, biasanya bakal muncul opsi dari bawah gitu kan? nah itu namana Bottom Sheet Dialog. Sebenernya banyak banget jenisnya, tapi kali ini aku mau bikin Bottom Sheet yang custom pake RecycleView juga.

Ini adalah tampilan akhir dari proyek yang akan kita buat.

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*YfT3gMyJv9P3eeSm4WcbLA.png"%}

Oke sebelum itu kita bakal tambahin beberapa library yang diperluin di file `build.gradle` proyek kalian.

{%- gist 7ca36e8d410173ea07bb30d116109417 %}

Oke mungkin kalian udah familiar dengan library di atas, jadi pada proyek kali ini kita bikin bottom sheet yang listnya kita buat menggunakan recycle view. Kenapa harus pake recycleview? Bukannya nanti nambah ribet? Hmmm engga sih sebenernya, malah ketika kita pake recycleview program kita bakal lebih fleksibel dan dinamis, dan irit kode juga sih hehe.

Oke langkah pertama kita bakal bikin xml item recycleviewnya dulu. Kita kasih nama `item_content.xml`, terus lengkapi kodenya jadi seperti ini.

{%- gist 13da2662817de84905bd94ca706dc34c %}

File item_content.xml di atas itu punya 2 komponen yaitu ImageView dan TextView, ini nanti kita gunain buat list item apa aja yang akan kita tampilkan. Di file di atas ada komponen sytle yang belum kita definisikan yaitu **ItemsTouchable**. Sytle ini digunakan buat bikin efek view kita seperti button bisa di klik gitu. Oke kita tambahkan style ini di file `style.xml`.

{%- gist 4c52ae98646fe39909e95ad7170657cc %}

Oke next kita bikin layout buat bottom sheetnya, di layout ini kita tambahkan 2 komponen juga yaitu TextView dan RecycleView, oke kita bikin layoutnya dengan nama `item_buttom_sheet.xml`, terus coba lengkapi filenya jadi seperti ini.

{%- gist 40052a21e785bc9f99a5770434fa6445 %}

Nah coba kita perhatiin kode di atas, di **ConstraintLayout** ada beberpa atribut yang kita tambahin, ini yang penting apa aja? coba perhatiin kode ini.

```xml
app:behavior_hideable="true"
app:behavior_peekHeight="56dp"
app:layout_behavior="com.google.android.material.bottomsheet.BottomSheetBehavior"
```

coba kita bedah satu-satu yak, di situ ada `app:behavior_hideable=”true”` kode ini artinya layout bottom sheet kita memiliki kemampuan buat bisa di sembunyikan. Selanjutnya `app:behavior_peekHeight=”56dp”` kode ini aritnya tinggi layout yang bakal keliatan pas awal itu 56dp, ini bisa kalian sesuaiin juga, tapi dokumentasi material desain merekomendasikan 56dp. Oke yang terakhir itu `app:layout_behavior` kode ini buat jadiin **ConstraintLayout** kita memiliki sifat dari bottom sheet material desain dengan nambahin `com.google.android.material.bottomsheet.BottomSheetBehavior` sebagai parameter. Ada satu komponen text juga belum kita definisikan yaitu `android:text=”@string/contact_me”` kita coba isi dengan value **“Contact me”** pada file `style.xml`.

Oke lanjut kita lengkapi layout di activity_main.xml biar jadi seperti ini.

{%- gist c6fcbbec76a3b65c6def2316a119e272 %}

Layout `activity_main.xml` kita berisiikan 2 komponen yaitu **ImageView** dan **Button** yang masing-masing kita lapisi dengan **CardView**, di mana **CardView** yang pertama bakal ngebungkus **ImageView** dan bikin gambar di dalamnya jadi bentuknya lingkaran. Sedangkan **Button** kita pake **TextView** yang dibungkus **CardView** juga, biar kece gitu.

Untuk lebih detail tentang **Custom Shape ImageView dengan CardView** bisa baca [disini](https://derysudrajat.github.io/blog/custom-shape-image) ya.

Oke mantapp kita udah setengah jalan. Sekarang mari kita ngoding logikanya hehe paling seru nih, petama kita buat kelas model buat item recycleview kita. Kasih nana filenya `ItemDialog.kt`, terus lengkapi jadi seperti ini.

{%- gist 2fb3c5a27f16e89fa470dc5625a608be %}

Jadi pada kelas model kita kali ini berisikan 3 atribut yaitu img, text, dan url. img ini akan berisikan url gambar icon buat item kita, text adalah judul itemnya, sementara url adalah url dari item yang bakal di tuju seperti akun instagram atau github kita.

Lanjut kita buat adapter list di bottom seet kita, buat kelas baru namanya `DialogAdapter.kt`, habis itu lengkapi jadi seperti ini.

{%- gist f3ee555e42644291563929adec16f675 %}

Pada method `onBindViewHolder` kita buat aksi ketika kita klik item, buat intent action view untuk redirect ke url dari item tersebut. Di sini juga kita pake Glide buat load url gambar ke `ImageView`.

Lanjut kita lengkapi kode di kelas `MainActivity.kt` jadi seperti ini.

{%- gist ef952c6e57eb4419944419ec3a66578f %}

Nah di tahap ini yang penting buat paham cara bikin Bottom Sheet Dialog, coba perhtaikan ketika callback setOnClickListener milik btnShare. Coba kita pahami langkah-langkahnya.

* Inflate layout bottom sheetnya. cara inflate layout ada di line 44, disana ada varibel view yang menampung layout inflaternya.
```kotlin
val view = layoutInflater.inflate(R.layout.item_bottom_sheet, null)
```
* Inisialisasi adapternya. Inisiasi adapter ada di line 45 dengan menggunakan DailogAdapter dengan parameter activity dan listnya.
```kotlin
val dialogAdapter = DialogAdapter(this@MainActivity, listItemDialog)
```
* untuk listnya bisa diliat pada kode atasnya, kita memanfaatkan mutableListOf yang listnya berisikan item dari ItemDialog, kalian bisa sesuaikan isi dari ItemDialognya sendiri seperti icon, text, dan urlnya.
```kotlin
val listItemDialog = mutableListOf(
    ItemDialog(
        getString(R.string.img_url_ig),
        getString(R.string.txt_ig),
        getString(R.string.url_ig)
    ),
    ItemDialog(
        getString(R.string.img_url_github),
        getString(R.string.txt_github),
        getString(R.string.url_github)
    ),
    ItemDialog(
        getString(R.string.img_url_medium),
        getString(R.string.txt_medium),
        getString(R.string.url_medium)
    ),
    ItemDialog(
        getString(R.string.img_url_wa),
        getString(R.string.txt_wa),
        getString(R.string.url_wa)
    )
)
```
* Setelah itu inisialisasi recycleview pada line 46–50
* Buat variabel baru yaitu dialog yang menampung kelas BottomSheetDialog dengan parameter this.
```kotlin
val dialog = BottomSheetDialog(this)
```
* Setelah itu isikan contentView dari variabel dialog dengan view yang sudah di inflate di awal, dan tampilkan.
```kotlin
dialog.setContentView(view)
dialog.show()
```

Oke kita ke tahap akhir, karena kita menggunakan **Glide** untuk load image dengan url, kita memerlukan akses internet, oleh karena itu jangan lupa tambahkan permission Internet pada android manifestnya.

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

Yeee kelar deh bikin bottom sheet dialog kali ini, sebenernya bikinnya gampang bet ya hehehe, ya karena kita bikin yang user friendly gitu biar asek ya ga hehe, so terima kasih udah baca post ini, untuk kode selengkapnya bisa liat di repo github ku di bawah ya, so sampe ketemu di post selantjunya dan seperti biasa **#ubahdengankode**.

Github Source [derysudrajat/custom-dialog](https://github.com/derysudrajat/custom-dialog)
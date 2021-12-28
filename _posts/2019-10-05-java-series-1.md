---
title: Tools | Java Series 1
tags: [Java, Technology]
style: fill
color: primary
description: Kita tahu dalam sebuah permainan, seorang penyihir (Mage / Wizard) adalah role yang selalu mempersiapkan perlengkapannya sebelum berperang. Begitupun dalam dunia programming kita sebagai developer memerlukan sebuah senjata yaitu tools yang kita gunakan dalam proses developing sebuah program.
---

Source: [Dery Sudrajat](https://medium.com/@dery.io/tools-java-series-1-cd326056725f)

{% include elements/figure.html image="https://miro.medium.com/max/1400/1*AM3SydGA9FWL6gqsLGgQ2A.png"%}

Kita tahu dalam sebuah permainan, seorang penyihir (Mage / Wizard) adalah role yang selalu mempersiapkan perlengkapannya sebelum berperang. Begitupun dalam dunia programming kita sebagai developer memerlukan sebuah senjata yaitu tools yang kita gunakan dalam proses developing sebuah program. Dalam hal ini yang pertama kita memerlukan sebuah Java Development Kit (JDK).

#### **Java Development Kit (JDK)**
Java Development Kit adalah tools yang digunakan seorang developer dalam proses developing, debugging, dan monitoring suatu aplikasi Java. Di dalam JDK juga terdapat Java Runtime Environment yang digunakan untuk menjalankan suatu aplikasi Java.

#### **Develop, Debug, dan Monitor**
Apa itu proses Develop?, **Develop** adalah proses penyusunan baris per baris kode program hingga menjadi satu aplikasi atau yang utuh dan memiliki suatu fungsi tertentu. Dalam proses ini kesalah mungkin akan terjadi, kesalah ini biasa disebut bug, bug sendiri adalah error yang dapat membuat sebuah aplikasi tidak dapat berjalan seperti yang fungsi yang diinginkan. Disinilah muncul sebuah istilah yaitu **Debug**, ialah proses untuk menghilangkan masalah tersebut kemudian memperbaiki sehingga program dapat berjalan seperti yang diinginkan. Kemudin **Monitor** adalah proses mengamatai jalannya aplikasi yang kita buat, proses monitor ini biasanya melakukan monitoring terhadap performa aplikasi dengan environment dimana ia dijalankan. Pada intinya JDK adalah tools wajib yang harus digunakan seorang Java Developer untuk membangun aplikasi dari awal hingga akhir.

#### **Integrated Development Environment (IDE)**
IDE (Integrated Development Environment) adalah program komputer yang memiliki beberapa fasilitas yang diperlukan dalam pembangunan perangkat lunak. Tujuan dari IDE adalah untuk menyediakan semua utilitas yang diperlukan dalam membangun perangkat lunak.

Sebuah **IDE**, atau secara bebas dapat diterjemahkan sebagai Lingkungan Pengembangan Terpadu, setidaknya memiliki fasilitas:

- **[Editor](https://id.wikipedia.org/wiki/Editor)**, yaitu fasilitas untuk menuliskan kode sumber dari perangkat lunak.
- **[Compiler](https://id.wikipedia.org/wiki/Compiler)**, yaitu fasilitas untuk mengecek sintaks dari kode sumber kemudian mengubah dalam bentuk binari yang sesuai dengan bahasa mesin.
- **[Linker](https://id.wikipedia.org/w/index.php?title=Linker&action=edit&redlink=1)**, yaitu fasilitas untuk menyatukan data binari yang beberapa kode sumber yang dihasilkan [compiler](https://id.wikipedia.org/wiki/Compiler) sehingga data-data binari tersebut menjadi satu kesatuan dan menjadi suatu program komputer yang siap dieksekusi.
- **[Debuger](https://id.wikipedia.org/w/index.php?title=Debuger&action=edit&redlink=1)**, yaitu fasilitas untuk mengetes jalannya program, untuk mencari [bug](https://id.wikipedia.org/wiki/Bug)/kesalahan yang terdapat dalam program.Sampai tahap tertentu IDE modern dapat membantu memberikan saran yang mempercepat penulisan.

Untuk membuat suatu aplikasi Java sebenarnya cukup dengan teks editor dan command line. Editor digunakan untuk menuliskan baris kodenya sementara command line digunakan untuk menjalankan perintah Java. Akan tetapi, saat ini sudah ada IDE yang membantu tidak hanya dalam proses developing, bahkan hingga optimasinya.

IDE juga biasanya dilengkapi dengan version control system yang bermanfaat untuk versioning suatu aplikasi. Beberapa IDE juga memiliki tools untuk membuat tampilan (layout) dalam Graphical User Interface (GUI), sehingga kita bisa membuat suatu tampilan dengan cara drag-and-drop.

IDE saat ini sudah menjadi tools wajib untuk memaksimalkan produktivitas seorang developer dalam membuat suatu aplikasi. Seperti perumpamaan sebelumnya, IDE adalah senjata developer. Semakin canggih dan tingginya kita menguasai senjata tersebut, semakin ampuh juga efeknya.

Tools yang akan digunakan di dalam series ini adalah :

- **OpenJDK**, yakni free open source di bawah lisensi **GNU** General Public License.
- **Intellij**, adalah IDE untuk Java development yang dikembangkan oleh JetBrains

Tanpa berlama-lama cus kita langsung coba install senjata yang kita perlukan dalam developing program java berikut.

#### How to install JDK

1. Unduh OpenJDK di tautan ini [http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html](http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html)
2. Langsung saja buka tautan di atas menggunakan browser Anda. Pilih Java Platform (JDK).

{% include elements/figure.html image="https://miro.medium.com/max/1096/0*rdLpMQwBG3F24IgJ"%}

Lalu pilihlah yang sesuai dengan gawai (device) dan OS yang Anda pakai. Jangan lupa untuk melakukan **Accept License Agreement**.

{% include elements/figure.html image="https://miro.medium.com/max/1086/0*jL5bNW5vTmXHFZSg"%}

Setelah proses mengunduh selesai, langsung instal ke gawai Anda dan ikuti petunjuknya sampai selesai.

#### How to install Intellij IDEA

1. Unduh Intellij di tautan ini [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/).(Anda bisa menggunakan versi Community) {% include elements/figure.html image="https://miro.medium.com/max/1400/1*zvMgcYB2lvPTiIuM8dQf0A.jpeg"%}
2. Jika sudah selesai mengunduh langsung run saja installer dan ikuti langkah-langkahnya. {% include elements/figure.html image="https://miro.medium.com/max/506/1*QtQnBxMpRBNRVZwNbtiSxA.jpeg"%}
3. Pilih Next > {% include elements/figure.html image="https://miro.medium.com/max/990/1*xIbUZiRnZhuKZPCamaLs4w.jpeg"%}
4. Pilih lokasi di mana aplikasi akan di simpan. {% include elements/figure.html image="https://miro.medium.com/max/990/1*YeATWWhXk_4xOh8BoAbsYQ.jpeg"%}
5. Cetang pilihan Update Path variable dan launcher sesuai dengan versi OS yang digunakan. {% include elements/figure.html image="https://miro.medium.com/max/994/1*g52_06rgbD6nxkJIwNGD_w.jpeg"%}
6. Untuk start menu biarkan pilihan default-nya tetap dan **install**. {% include elements/figure.html image="https://miro.medium.com/max/988/1*0l4gy_qGrJFBzSdbXIJlWg.jpeg"%}
7. Tunggu hingga proses instalasi selesai. {% include elements/figure.html image="https://miro.medium.com/max/990/1*ERSMgqmZurtBIXd9OoUd5g.jpeg"%}
8. ketika selesai pilih Reboot now atau Reboot later sesuaikan dengan kondisi anda, setelah itu klik **Finish**. {% include elements/figure.html image="https://miro.medium.com/max/990/1*smTPG7PnkSIW9wYBcXXSVw.jpeg"%}

Untuk petunjuk pemakaian yang resmi dari Intellij, silakan lihat tautan ini [https://www.jetbrains.com/help/idea/meet-intellij-idea.html](https://www.jetbrains.com/help/idea/meet-intellij-idea.html).

Tunggu chapter selanjutnya di Java series yaa…


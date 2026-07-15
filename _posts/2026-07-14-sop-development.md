---
layout: post
title: SOP Development
---


## Penggunaan Bahasa
1. Penamaan variable, class, method dan dokumentasi pada kode program secara default menggunakan bahasa Inggris.
2. Penamaan tabel dan kolom pada database secara default menggunakan bahasa Inggris tanpa menggunakan prefix / suffix. Aturan penamaan sebagai berikut:
* <strong>Plural noun</strong> (misal: users, products dan classes) untuk nama tabel
* <strong> Singular noun</strong> (misal: name, email dan password) untuk nama kolom / atribut.
3. Penggunaan bahasa pada tampilan antar muka aplikasi (misal: navigasi, tabel, tombol dan dialog) secara default menggunakan bahasa Indonesia.
4. Setiap aturan penggunaan bahasa yang tercantum pada poin "1" sampai "3" di atas dapat disesuaikan dengan permintaan dari product owner / client.
5. Setiap aturan penggunaan bahasa yang tercantum pada poin "1" sampai "2" di atas harus diterapkan secara konsisten dan menyeluruh.

## Konvensi Penulisan kode
1. Standar gaya penulisan kode yang digunakan untuk bahasa pemrograman <strong>PHP</strong> adalah <a href=http://www.php-fig.org/psr/psr-2>PSR-2.</a>
2. Standar gaya penulisan kode yang digunakan untuk bahasa pemrograman <strong>JAVA / Android </strong>adalah <a href="https://google.github.io/styleguide/javaguide.html">Google Java Style.</a>



## Version Control System (VCS)
1. Setiap kode yang dibuat dengan tujuan untuk pengerjaan proyek internal BPN Kota Malang wajib disimpan ke dalam Repository Github BPN Kota Malang yang sementara beralamat di https://github.com/Internal-BPN-Kota-Malang.
2. Setiap repository kode proyek internal BPN Kota Malang yang tersimpan di server Github BPN Kota Malang wajib dimasukkan kedalam group BPN KOta Malang yang terletak di alamat https://github.com/Internal-BPN-Kota-Malang.
3. Setiap repository kode proyek komersial dan internal BPN Kota Malang sekurang-kurangnya memiliki 2 (dua) buah branch yang diantaranya adalah:
* <strong>Main</strong>: Branch "master" pada git ditujukan untuk "stable code" yang siap diberikan atau direview oleh product owner / client.
* <strong>Develop</strong>: Branch "develop" pada git ditujukan untuk kegiatan pengembangan sehari-hari dan tidak direkomendasikan untuk diberikan ke orang lain selain programmer.
4. Apabila ditemukan <strong>defect</strong> atau terjadi <Strong>failure</strong> pada kode yang berada di branch <strong>main</strong> maka perlu diberlakukan mekanisme <strong>hotfix</strong> dengan cara membuat branch <strong>hotfix</strong>yang bersumber dari <strong>HEAD</storng> branch <strong>main</strong>.
5. Setiap branch <strong>hotfix</strong> yang telah berhasil memperbaiki defect atau failure pada branch master harus digabungkan kembali dengan branch master melalui mekanisme merge dari branch <strong>hotfix</strong> ke branch <strong>main </strong>.
6. Setelah selesai melakukan hotfix pada branch master, branch develop harus mendapatkan perubahan terakhir pada branch <strong>main </strong> dengan cara melakukan proses <strong>merge</strong> dari branch <strong>main</strong>ke branch <strong>develop</strong>.

## Version Number
1. Setiap aplikasi yang dibuat untuk keperluan proyek komersial dan internal BPN Kota Malang diharuskan memiliki version number.
2. Format dari version number yang digunakan oleh BPN KOta Malang adalah format dari Semantic Versioning 2.0.0 (SemVer 2.0.0) dengan pola X.Y.Z yang memiliki arti:
* <strong>X (Major Version)</strong>: Merupakan versi yang diberikan kepada aplikasi pada saat melakukan perubahan yang berdampak pada arsitektur, framework ataupun core dari aplikasi yang bersangkutan.
* <strong>Y (Minor Version)</strong>: Merupakan versi yang diberikan kepada aplikasi pada saat melakukan penambahan, pengubahan atau penghapusan sebuah fitur.
* <strong>Z (Patch Version)</strong>: Merupakan versi yang diberikan kepada aplikasi pada saat melakukan perbaikan (bug fixing) pada sebuah fitur.
3. Setiap aplikasi yang dibuat dimulai dengan versi <strong>0.1.0</strong> dan akan berubah menjadi versi <strong>1.0.0</strong> ketika sudah siap diberikan kepada product owner / client dan masuk ke fase production untuk yang pertama kalinya.
4. Kenaikan versi hanya terjadi apabila project manager sudah menyepakati bahwa aplikasi yang dibuat sudah layak untuk di-release / dipresentasikan kepada product owner / client.
5. Setiap terjadi kenaikan versi pada sebuah aplikasi, developer diharuskan untuk membuat "annotated tagging" dengan nama sesuai dengan nomor revisi terakhir dengan format vX.Y.Z (misal v1.1.4) pada HEAD milik branch "main".
6. Setiap terjadi kenaikan versi pada sebuah aplikasi, developer diharuskan untuk membuat changelog perubahan yang terjadi yang disimpan didalam berkas bernama "changelog" atau "changelog.txt" yang berisi tentang perubahan apa saja yang terjadi dari versi sebelumnya seperti contoh dibawah ini: 
{% highlight js %}
Changelog:

 Ver. 1.2.1
 Perbaikan bug saat mengirim email notifikasi pada modul salary untuk HR Manager.
 Security fix SQL Injection pada halaman login.

 Ver. 1.2.0
 Penambahan fitur export to excel pada modul laporan keuangan
 Penambahan modul salary untuk HR Manager.

 Ver. 1.9.24
 Security fix: Menganggulangi CSRF dengan cara mengimplementasikan CSRF token pada setiap request bertipe POST.
{% endhighlight %}

## Penjaminan Mutu
1. Setiap developer diharuskan untuk menjalankan mekanisme software testing pada bagian kode yang dibuatnya sampai pada tahap developer tersebut memiliki kepercayaan diri bahwa bagian kode dibuatnya dapat bekerja sesuai dengan ekspektasi.
2. Setiap developer diharuskan untuk mendokumentasikan kegiatan software testing yang dilakukannya untuk kemudian dijadikan sebagai bukti bahwa bagian kode yang dibuat sudah lulus dari proses software testing.

## Dokumentasi
1. Setiap developer diharuskan untuk membuat kode yang mudah dipelajari oleh pengembang lain.
2. Setiap developer diharuskan untuk membuat kode yang mudah dipelajari oleh pengembang lain.
3. Setiap method yang dibuat harus memiliki dokumentasi yang sekurang-kurangnya menjelaskan hal - hal berikut ini:
* Tujuan utama dari method yang dibuat.
* Parameter yang dibutuhkan.
* Return value yang akan diberikan.
4. Format penulisan dokumentasi program harus konsisten dan seragam dalam satu aplikasi yang sama.
5. Format penulisan dokumentasi program harus konsisten dan seragam dalam satu aplikasi yang sama.
6. Penulisan dokumentasi untuk method yang memiliki nama dan fungsi yang sederhana dan jelas seperti misalnya (`<getAddress>`, `<getName>` dan `<getEmail>`) bersifat opsional. Akan tetapi, jika method yang dibuat "terlihat" sederhana dan jelas namun memiliki logic atau prosedur yang tidak biasa, maka penulisan dokumentasi menjadi hal yang diharuskan.
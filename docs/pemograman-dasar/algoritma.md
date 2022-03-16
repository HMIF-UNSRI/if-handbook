---
sidebar_position: 1
slug: /perkenalan-algoritma
---

# A.1 Algoritma

## Perkenalan Algoritma

Dalam dunia pemograman, salah satu kemampuan dasar dan penting yang diperlukan adalah **_Problem Solving_**. Dalam
menyelesaikan permasalahan, kita memerlukan teknik untuk menyelesaikanya, atau disebut juga sebagai Algoritma.

Algoritma adalah urutan atau langkah-langkah untuk menyelesaikan suatu permasalahan, algoritma biasanya
diimplementasikan menggunakan bahasa pemograman.

## Siklus Algoritma

Algoritma memiliki siklus yang berulang, seperti berikut :

1. **Masalah**, algoritma dibuat karena adanya suatu permasalahan, sebab itu langkah pertama yang diperlukan ialah
   mendeskripsikan permasalahan yang dihadapi.
2. **Solusi**, setelah mengetahui detail permasalahan cobalah untuk memikirkan solusi dari permasalahan tersebut, salah
   satu cara yang paling efeketif adalah mengubah masalah menjadi bagian-bagian kecil, dan menyelesaikanya satu persatu.
3. **Implementasi**, apabila semua permasalahan sudah didapatkan solusinya, maka langkah selanjutnya adalah menentukan
   teknologi yang akan digunakan sebagai media implementasi.
4. **Uji Coba**, tidak selalu solusi yang dihasilkan merupakan hal yang benar atau tidak efektif, terkadang terdapat
   beberapa kesalahan yang tidak disadari sebagai contoh ingin menyelesaikan masalah pengakaran suatu angka dan pada
   solusi sebelumnya kita belum menangani permasalah yang muncul apabila angka bernilai negatif. Dengan adanya tahap ini
   kita bisa melakukan improve terhadap solusi kita sebelumnya.

## Contoh Permainan

Berikut contoh permainan yang menggambarkan bagaimana cara berpikir secara terurut dan efisien.

- [Tower of Hanoi](https://www.mathsisfun.com/games/towerofhanoi.html), permainan ini menuntut kalian untuk
  menyelesaikan permasalahan pemindahan seluruh kaset pada tower ke-3 dengan gerakan memindah seminimal mungkin.
  Permainan ini baik untuk melatih kemampuan pemecahan masalah kalian karena dituntut untuk berpindah se-efisien
  mungkin.

- [The Mind Reader](https://www.mathsisfun.com/games/mind-reader.html), permainan kali ini akan mencoba untuk menebak
  angka yang ada pada pikiran kalian, cobalah untuk menemukan algoritma dibelakang layar pada permainan ini !

## Notasi Algoritma

Terdapat tiga notasi yang sering digunakan sebagai cara penulisan dari pembuatan algoritma.

### A. Kalimat Deskriptif

Metode ini digunakan dengan cara menuliskan instruksi-instruksi yang harus dilaksanakan dalam bentuk untaian kalimat
deskriptif dengan bahasa yang jelas, mudah dimengerti, dan terurut. Gambaran kasar dari metode ini adalah seperti
hal-nya teks prosedur, contoh :

```text
Program Masuk Akun

Algoritma :
1. Masukkan email dan password
2. Verifikasi apakah email sudah terdaftar pada penyimpanan
    a. Jika terdaftar, periksa password yang terikat pada email apakah cocok dengan password masukkan
        - Jika cocok, berhasil masuk
        - Jika tidak, tampilkan kesalahan
    b. Jika tidak, tampilkan kesalahan
```

### B. Flowchart

Flowchart adalah cara menuliskan instruksi-instruksi yang harus dilaksanakan dalam bentuk simbol-simbol diagram alir.
Terdapat banyak standar untuk menuliskan flowchart sehingga tidak ada ketetapan dalam membuatnya, tujuan utama dari
flowchart adalah menggambarkan proses-proses, selama itu mudah dipahami, maka tidak mengikuti standar baku juga tidak
masalah. Akan tetapi terdapat beberapa simbol yang sering digunakan, sehingga simbol-simbol tersebut sudah seperti
standar baku. Berikut merupakan simbol-simbol yang biasa digunakan pada flowchart :

| Simbol                                                                                                                                     | Nama          | Fungsi                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------|
| ![terminator](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/flowchart-symbols-meaning-explained/terminator_symbol-60x31.PNG) | Terminator    | Memulai dan mengakhiri Flowchart                                        |
| ![process](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/flowchart-symbols-meaning-explained/process_symbol-60x45.PNG)       | Proses        | Melakukan sebuah aksi, proses, atau fungsi                              |
| ![io](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/flowchart-symbols-meaning-explained/data_symbol-60x46.PNG)               | Data          | Melakukan input/output                                                  |
| ![decision](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/flowchart-symbols-meaning-explained/decision_symbol-60x46.PNG)     | Pengkondisian | Menentukan kondisi suatu pernyataan, biasanya bernilai benar atau salah |

Baca lebih lengkap pada halaman
berikut [LucidChart](https://www.lucidchart.com/pages/flowchart-symbols-meaning-explained#section_0)

Untuk membuat flowchart terdapat banyak situs atau software gratis yang dapat digunakan, diantaranya adalah :

1. [LucidChart](https://www.lucidchart.com)
2. [draw.io](https://app.diagrams.net)
3. [FigmaJam](https://www.figma.com)

Contoh flowchart dari algoritma Masuk Akun :
<img src="/img/flowchart.png" alt="contoh-flowchart" width="350"/>

### C. Pseudocode

Pseudocode adalah langkah-langkah pemecahan masalah dengan menggunakan kode yang tidak terikat pada bahasa pemrograman
tertentu. Biasanya pseudocode digunakan untuk gambaran kasar alur program semirip mungkin dengan bahasa pemograman akan
tetapi dibuat semirip mungkin dengan bahasa pemograman. Sama seperte flowchart, pseudocode juga tidak memiliki standar
baku.

Terdapat beberapa sintaks yang biasanya digunakan pada pseudocode yaitu :

- DECLARE, untuk mendefinisikan variabel
- INPUT, untuk memasukkan data
- DISPLAY, untuk menampilkan data
- IF ELSE, untuk mengkondisian
- FOR, untuk perulangan
- SET, untuk mengubah nilai

Contoh :

```text
DECLARE string email, password

INPUT email, password
IF email is valid THEN check password
    IF password is valid THEN DISPLAY "Success Page"
    ELSE DISPLAY "Failed Page"
ELSE DISPLAY "Failed Page"
```
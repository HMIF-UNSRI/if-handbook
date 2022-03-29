---
sidebar_position: 4
slug: /tipe-data-primitif
---

# A.4 Tipe Data Primitif

Tipe data merupakan salah satu konsep dasar dalam pemrograman. Java memiliki beberapa tipe data baik berupa numerik,
string, dan boolean.

## Tipe Data Angka

Tipe data pada angka pada Java dibagi menjadi 2 yaitu Bilangan Bulat (Integer Number), dan Bilangan Koma (Floating Point
Number).

### Bilangan Bulat

Terdapat 4 tipe data integer number pada Java, yaitu sebagai berikut :

| Tipe Data  | Minimal                    | Maksimal                  | Ukuran  | Default |
|------------|----------------------------|---------------------------|---------|---------|
| `byte`     | -128                       | 127                       | 1 byte  | 0       |
| `short`    | -32,768                    | 32,767                    | 2 bytes | 0       |
| `int`      | -2,147,483,648             | 2,147,483,647             | 4 bytes | 0       |
| `long`     | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 | 8 bytes | 0       |

Contoh penerapan kode:

```java
byte angkaByte = 100;
short angkaShort = 1_000;
int angkaInt = 100_000;
long angkaLong = 100_000_000_000L;
```

Perhatikan pada tipe data `long`, terdapat karakter `L` pada nilai angka, hal itu dikarenakan secara default Java
menganggap kita membuat tipe data `int` dan kita perlu memberikan tanda `L` bila ingin mendifinisikan `long`.

Selain itu, pada kode diatas kita membuat **underscore**, hal itu untuk mempermudah kita dalam membaca nilai tersebut.
Tanpa underscore kita juga akan mendapatkan nilai yang sama. Fitur **underscore** terdapat pada Java versi 7 keatas,
pastikan versi kalian kompatibel agar dapat menggunakan underscore.

### Bilangan Koma

Terdapat 2 tipe data floating number number pada Java, yaitu sebagai berikut :

| Tipe Data | Minimal  | Maksimal | Ukuran  | Default |
|-----------|----------|----------|---------|---------|
| `float`   | 3.4e-038 | 3.4e+038 | 4 bytes | 0.0     |
| `double`  | 1.7e-308 | 1.7e+308 | 8 bytes | 0.0     |

Contoh penerapan kode:

```java
float angkaByte = 100.5F;
double angkaShort = 12.55;
```

Perhatikan pada tipe data `float`, terdapat karakter `F` pada nilai angka, hal itu dikarenakan secara default Java
menganggap kita membuat tipe data `double` dan kita perlu memberikan tanda `F` bila ingin mendifinisikan `float`.


Setelah mengetahui berbagai tipe data angka, silahkan pilih tipe data sesuai rentang yang kalian butuhkan. Biasanya banyak orang menggunakan tipe data `int` sebagai bilangan bulat, akan tetapi jika kalian membutuhkan rentang angka melebihi `int` silahkan gunakan `long`, apabila rentang angka yang dibutuhkan juga masih kurang, terdapat tipe data `BigInteger` yang tidak akan dibahas pada sesi ini.

## Tipe Data Boolean
Tipe data boolean merupakan tipe data yang hanya dapat bernilai benar atau salah. Untuk melambangkan benar dengan sintaks `true`, dan salah untuk `false`. Nilai default dari boolean adalah false.
```java
boolean benar = true;
boolean salah = false;
boolean nilaiDefault;

System.out.println(benar);
System.out.println(salah);
System.out.println(nilaiDefault);
```

<pre>
  <b>Output: </b>{'\n'}true{'\n'}false{'\n'}false
</pre>

## Tipe Data Character
Tipe data character merupakan tipe data yang bernilai satu huruf. Untuk menuliskan tipe data character menggunakan sintaks `char` dan nilainya menggunakan tanda petik `''`.
```java
char nilaiUjian = 'A';
System.out.println(nilaiUjian);
```
<pre>
  <b>Output: </b>A
</pre>

## Tipe Data String
Tipe data string merupakan tipe data yang berisikan kumpulan karakter atau kalimat, sintaks untuk menuliskan tipe data string adalah `String` dan nilainya menggunakan kutip dua `""`. Nilai default dari string adalah `null`.
```java
String nama = "Giorno Giovanna";
String nim = "090000";
String namaNim = nama + " " + nim;
System.out.println(namaNim);
```
<pre>
  <b>Output: </b>Giorno Giovanna 090000
</pre>
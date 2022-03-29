---
sidebar_position: 5
slug: /variabel
---

# A.5 Variabel

Variabel adalah tempat menampung nilai dari suatu data. Java merupakan bahasa static yang dimana artinya suatu variabel hanya dapat menampung tipe data yang sama, kita tidak dapat mengubah nilai dari angka menjadi kalimat, hanya dapat dari angka menjadi angka atau tipe data yang sama.

Untuk membuat tipe data pada Java kita dapat menuliskanya dengan kata kunci tipe data, lalu nama variabel, dan terakhir nilai datanya, contoh :
```text
<tipe data> <nama variabel> = <nilai data>
```
```java
int nilaiUjian;
nilaiUjian = 100;

String nama = "Eren Yeager";

System.out.println(nilaiUjian);
System.out.println(nama);
```
<pre>
  <b>Output: </b>{'\n'}100{'\n'}Eren Yeager
</pre>

### Kata kunci `final`
Sebelumnya, kita membuat suatu variabel yang nilai nya dapat berubah-ubah sesuai tipe data-nya. Adakalanya kita ingin membuat suatu nilai data yang pasti atau tidak akan pernah berubah nilainya, atau disebut juga sebagai konstan. Pada java untuk membuat suatu variabel konstan, dapat menggunakan kata kunci `final`.
```java
final String bahasa = "Indonesia";
bahasa = "Inggris" // Error
System.out.println(bahasa);
```
<pre>
  <b>Output: </b> Indonesia
</pre>
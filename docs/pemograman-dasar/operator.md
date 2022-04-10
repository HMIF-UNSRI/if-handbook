---
sidebar_position: 8
slug: /operator
---

# A.8 Operator

## Operator Aritmatika

Operator aritmatika digunakan untuk melakukan operasi matematika dasar.

| Operator | Keterangan     |
|----------|----------------|
| +        | Penjumlahan    |
| -        | Pengurangan    |
| *        | Perkalian      |
| /        | Pembagian      |
| %        | Sisa Pembagian |

```java title="../src/Main.java"
public class Main {
    public static void main(String[] args) {
        int a = 100;
        int b = 10;
        System.out.println(a + b);
        System.out.println(a - b);
        System.out.println(a * b);
        System.out.println(a % b);
    }
}
```

<pre>
  <b>Output: </b>{'\n'}110{'\n'}90{'\n'}1000{'\n'}10{'\n'}0
</pre>

## Operator Penugasan

Operator penugasan (Assignment Operator) fungsinya untuk meberikan tugas pada variabel tertentu. Biasanya untuk mengisi
nilai. Kita bisa menyingkat penulisan sintask, misal dari `a = a + 10` menjadi `a += 10`.

| Operasi Matematika | Operator Penugasan |
|--------------------|--------------------|
| a = a + 10         | a += 10            |
| a = a - 10         | a -= 10            |
| a = a * 10         | a *= 10            |
| a = a / 10         | a /= 10            |
| a = a % 10         | a %= 10            |
| a = a + 1          | a++                |
| a = a - 1          | a--                |

```java title="../src/Main.java"
public class Main {
    public static void main(String[] args) {
        int a = 100;
        
        a += 10;
        System.out.println(a);
        
        a -= 10;
        System.out.println(a);
        
        a *= 10;
        System.out.println(a);
        
        a++;
        System.out.println(a);
    }
}
```

<pre>
  <b>Output: </b>{'\n'}110{'\n'}100{'\n'}1000{'\n'}1001
</pre>

## Operator Pembanding

Operasi perbandingan adalah operasi untuk membandingkan dua buah data yang menghasilkan nilai boolean (benar atau salah)
. Jika hasil operasinya adalah benar, maka nilainya adalah `true`,dan Jika hasil operasinya adalah salah, maka nilainya
adalah `false`

| Operater    | Keterangan              |
|-------------|-------------------------|
| >           | Lebih dari              |
| <           | Kurang dari             |
| > =         | Lebih dari sama dengan  |
| <=          | Kurang dari sama dengan |
| ==          | Sama dengan             |
| !=          | Tidak sama dengan       |
| `.equals()` | Sama dengan (String)    |


```java title="../src/Main.java"
public class Main {
    public static void main(String[] args) {
        int value1 = 100;
        int value2 = 100;
        
        System.out.println(value1 > value2);
        System.out.println(value1 < value2);
        System.out.println(value1 >= value2);
        System.out.println(value1 <= value2);
        System.out.println(value1 == value2);
        System.out.println(value1 != value2);
    }
}
```

<pre>
  <b>Output: </b>{'\n'}false{'\n'}false{'\n'}true{'\n'}true
</pre>

Untuk membadingkan sebuah string, sedikit berbeda dengan tipe data lain, kita tidak bisa menggunakan `==` karena operator tersebut membandingkan lokasi memori pada komputer jika digunakan pada objek, oleh karena itu gunakan `.equals()` untuk membadingkanya, lihat contoh dibawah.



## Operator Boolean

Operator boolean digunakan untuk melakukan suatu operasi logika. Operasi ini terkait dengan materi Logika Matematika
atau Gerbang Logika. Baca lebih lengkap mengenai Logika
Matematika [disini](https://pahamify.com/blog/pahami-materi/materi-matematika/materi-logika-matematika-kelas-11/).

| Operator | Keterangan        |
|----------|-------------------|
| &&       | Dan               |
| II       | Atau              |
| !        | Kebalikan         |

### Operasi && (Dan)

| Nilai 1 | Operator | Nilai 2 | Hasil |
|---------|----------|---------|-------|
| true    | &&       | true    | true  |
| true    | &&       | false   | false |
| false   | &&       | true    | false |
| false   | &&       | false   | false |

### Operasi || (Atau)

| Nilai 1 | Operator | Nilai 2 | Hasil  |
|---------|----------|---------|--------|
| true    | II       | true    | true   |
| true    | II       | false   | true   |
| false   | II       | true    | true   |
| false   | II       | false   | false  |

### Operasi ! (Negasi)

| Operator | Nilai | Hasil |
|----------|-------|-------|
| !        | true  | false |
| !        | false | true  |

## Contoh

Kita akan mencoba sebuah contoh sederhana yaitu Sistem Login, biasanya ketika kita ingin masuk ke sebuah platform, kita
menggunakan akun yang terdiri dari email dan kata sandi. Buatlah sebuah operasi yang benar agar sistem login kita
bekerja dengan baik.

Jawab :

Untuk berhasil login, membutuhkan **email yang benar** dan **kata sandi yang benar**.

Apabila di notasikan, maka akan menjadi `email ^ password`, sehingga kita bisa membuat kode programnya seperti berikut.

```java title="../src/Main.java"
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String emailTersimpan = "hmifunsri@gmail.com";
        String passwordTersimpan = "BphAkademikTamvan99";
        
        String emailInput = scanner.nextLine();
        String passwordInput = scanner.nextLine();
        
        boolean isEmailMatch = (emailTersimpan.equals(emailInput));
        boolean isPasswordMatch = (passwordTersimpan.equals(passwordInput));
        
        System.out.println(isEmailMatch && isPasswordMatch);
    }
}
```
Contoh semua benar :
<pre>
  <b>Input: </b>{'\n'}hmifunsri@gmail.com{'\n'}BphAkademikTamvan99
</pre>

<pre>
  <b>Output: </b>true
</pre>

Contoh salah satu benar :
<pre>
  <b>Input: </b>{'\n'}hmifunsri@gmail.com{'\n'}salahPassword
</pre>

<pre>
  <b>Output: </b>false
</pre>

Contoh semua salah :

<pre>
  <b>Input: </b>{'\n'}salahEmail{'\n'}salahPassword
</pre>

<pre>
  <b>Output: </b>false
</pre>
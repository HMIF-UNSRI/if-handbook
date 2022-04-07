---
sidebar_position: 6
slug: /scanner-input
---

# A.6 Scanner Input

Terkadang kita tidak memasukkan nilai dalam suatu kode secara langsung, akan tetapi meminta user untuk memasukkan nilai.
Scanner merupakan objek bawaan java yang berfungsi sebagai penerima masukkan dari user.

Untuk menggunakan `Scanner`, pertama lakukan import pada kode program paling atas seperti berikut.

```java
import java.util.Scanner;
```

Selanjutnya inisialisasi objek scanner seperti berikut.

```java
Scanner scanner = new Scanner(System.in);
```

Jika kalian menggunakan IDE seperti IntelijIDEA, maka ketika mengetikkan `Scanner`, maka IDE akan memberikan anda
autocomplete yaitu objek Scanner, lalu tekan enter dan IDE akan secara otomatis melakukan import, sehingga kita tidak
perlu melakukan import seperti pada langkah sebelumnya.

Kode program lengkap :

```java title="../src/Main.java"
// highlight-next-line
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // highlight-next-line
        Scanner scanner = new Scanner(System.in);
    }
}
```

Terdapat beberapa fungsi dari objek `Scanner`yang dapat digunakan untuk menerima masukkan data dari user

| Method          | Deskripsi                                                  |
|-----------------|------------------------------------------------------------|
| `nextBoolean()` | Membaca nilai bertipe data `boolean` dari user             |
| `nextInt()`     | Membaca nilai bertipe data `int` dari user                 | 
| `nextFloat()`   | Membaca nilai bertipe data `float` dari user               |
| `next()`        | Membaca nilai bertipe data `string` dari user tanpa spasi  |
| `nextLine()`    | Membaca nilai bertipe data `string` dari user dengan spasi |
| `nextByte()`    | Membaca nilai bertipe data `byte` dari user                |
| `nextShort()`   | Membaca nilai bertipe data `short` dari user               |
| `nextLong()`    | Membaca nilai bertipe data `lomg` dari user                |
| `nextDouble()`  | Membaca nilai bertipe data `double` dari user              |

## Number

Kita dapat meminta masukkan dari user berupa angka baik integer ataupun floating-point. Berikut contoh meminta masukkan
angka umur.

```java title="../src/Main.java"
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan umur anda : ");
        // highlight-next-line
        int umur = scanner.nextInt();
        
        System.out.println("Umur saya " + umur + " tahun");
    }
}
```

<pre>
  <b>Input: </b>{'\n'}Masukkan umur anda : 17
</pre>

<pre>
  <b>Output: </b>Umur saya 17 tahun
</pre>

## String

Terdapat 2 cara untuk mendapatkan masukkan berupa string dari user, yaitu menggunakan `next()` atau `nextLine()`.

### `next()`

`next()` digunakan apabila kita memasukkan string tanpa spasi, jika kita menggunakan spasi, maka karakter spasi dan
setelahnya tidak akan dibaca.

```java title="../src/Main.java"
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // highlight-next-line
        String kata = scanner.next();
        
        System.out.println(kata);
    }
}
```

<pre>
  <b>Input: </b>Eren Yeager
</pre>

<pre>
  <b>Output: </b>Eren
</pre>

### `nextLine()`

`nextLine()` digunakan apabila kita memasukkan string menggunakan spasi, jika kita menggunakan spasi.

```java title="../src/Main.java"
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // highlight-next-line
        String kata = scanner.nextLine();
        
        System.out.println(kata);
    }
}
```

<pre>
  <b>Input: </b>Eren Yeager
</pre>

<pre>
  <b>Output: </b>Eren Yeager
</pre>

## Character

Untuk mengambil input karakter, dapat menggunakan fungsi `next()` dengan tambahan fungsi `charAt()`.

```java title="../src/Main.java"
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // highlight-next-line
        char karakter = scanner.next().charAt(0);
        
        System.out.println(karakter);
    }
}
```

<pre>
  <b>Input: </b>y
</pre>

<pre>
  <b>Output: </b>y
</pre>
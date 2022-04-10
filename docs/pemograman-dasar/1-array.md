---
sidebar_position: 11
slug: /perkenalan-array
---

# A.11 Array 1 Dimensi

## Apa Itu Array
Array merupakan sebuah variabel yang dapat menyimpan banyak data dalam satu variabel. Tipe data yang disimpan dalam suatu array harus bertipe sama. Array menggunakan indeks untuk mengakses data-data yang disimpannya. 


## Struktur Array

![StrukturArray](https://ds055uzetaobb.cloudfront.net/image_optimizer/7bfe2713ecaf427164d14018608b826ffbeea531.jpg)



## Deklarasi, Instantiasi, Inisialisasi

### Deklarasi
Deklarasi array pada java hampir sama seperti deklarasi variabel biasa. Hanya perlu ditambahkan kurung siku ([]) setelah tipe data atau setelah nama variabel (nama array).

```java
package main;
public class Main(){
  public static void main(String[] args){
    String[] buahBuahan ;
    String sayurSayuran[];
  }
}
```

### Instantiasi
Instantiasi array dapat dilakukan dengan menambahkan keyword new dan diikuti tipe data dengan
[(banyaknya elemen )]

```java
package main;
public class Main(){
  public static void main(String[] args){
    String[] buahBuahan = new String[5];
    String sayurSayuran[] = new String[5];
  }
}
```

### Inisialisasi
Inisialisasi array dapat dilakukan dengan langsung menginputkan data saat deklarasi array.

```java
package main;
public class Main(){
  public static void main(String[] args){
    String[] buahBuahan = {"apel", "pisang", "semangka"}
    String sayurSayuran[] = {"bayam", "kangkung", "sawi"}
  }
}
```

## Pengaksesan Array
Pengaksesan Array pada java dapat dilakukan dengan memanfaatkan index array.
Jika index diakses berada di luar range array yang dibuat maka akan menimbulkan Range Out Of Bound Error

```java
package main
public class AksesArray{
  public static void main(String[] args){
    String[] buahBuahan = {"jeruk", "semangka", "melon", "pisang"};
  
    // Mengakses Array
    System.out.println("Element Pertama " + buahBuahan[0]);
    System.out.println("Element Kedua   " + buahBuahan[1]);
    System.out.println("Element Ketiga  " + buahBuahan[2]);
    System.out.println("Element Keempat " + buahBuahan[3]);

    // Error Out Of Bound
    /*
    System.out.println("Element Keempat " + buahBuahan[3]);
    */
  }
}
```

Output:
```sh
Element Pertama jeruk
Element Kedua   semangka
Element Ketiga  melon
Element Keempat pisang
```

## Array Class
Package java.util.Arrays menyediakan method - method yang berguna untuk melakukan pemrosesan atau memanipulasi array. 
Implementasinya dapat langsung dengan import package tersebut di class secara langsung.
Berikut merupakan list method - method yang dapat dipakai

### `Arrays.sort()`
Mengurutkan array secara menaik berdasarkan natural ordering dari elemen tersebut.

```java
package main
import java.util.Arrays;

public class AksesArray{
  public static void main(String[] args){
    String[] buahBuahan = {"jeruk", "semangka", "melon", "pisang"};

    // Array Sebelum Di Sorting
    System.out.println("Unsorted Array");
    System.out.println("Element Pertama " + buahBuahan[0]);
    System.out.println("Element Kedua   " + buahBuahan[1]);
    System.out.println("Element Ketiga  " + buahBuahan[2]);
    System.out.println("Element Keempat " + buahBuahan[3] + "\n");

    Arrays.sort(buahBuahan);

    // Array Sesudah Di Sorting
    System.out.println("Sorted Array");
    System.out.println("Element Pertama " + buahBuahan[0]);
    System.out.println("Element Kedua   " + buahBuahan[1]);
    System.out.println("Element Ketiga  " + buahBuahan[2]);
    System.out.println("Element Keempat " + buahBuahan[3]);
  }
}
```

Output:
```sh
Unsorted Array
Element Pertama jeruk
Element Kedua   semangka
Element Ketiga  melon
Element Keempat pisang

Sorted Array
Element Pertama jeruk
Element Kedua   melon
Element Ketiga  pisang
Element Keempat semangka
```

### `Arrays.binarySearch()`

Mencari elmeen pada array menggunakan metode aljavaritma binary search. Array yang ingin dicari sebelumnya harus sudah di diurutkan terlebih dahulu. jika ada lebih dari satu elemen sama yang dicari, maka index yang dikembalikan tidak menentu

```java
package main
import java.util.Arrays;

public class AksesArray{
  public static void main(String[] args){
    String[] buahBuahan = {"jeruk", "semangka", "melon", "pisang"};
    Arrays.sort(buahBuahan);

    String key = "pisang";
    int index = Arrays.binarySearch(buahBuahan, "pisang");

    System.out.println(Arrays.toString(buahBuahan));
    System.out.println("Elemen " + key + " Berada di Index " + index);
  }
}
```

Output:

```sh
[jeruk, melon, pisang, semangka]
pisang Berada di Index 2
```

### `Arrays.equals()`

Memeriksa 2 buah array apakah sama satu dengan lainnya.  2 buah array dapat dikatakan sama apabila memiliki jumlah elemen yang sama dan semua element di index yang bersesuaian dari kedua array tersebut sama

```java
package main
import java.util.Arrays;

public class AksesArray{
  public static void main(String[] args){
    int[] nilaiWoody = {70,80,45,85};
    int[] nilaiBuzz = {70,80,45,85};
    int[] nilaiAndy = {80,70,85,45};

    System.out.println("Woody : Buzz = " + Arrays.equals(nilaiWoody, nilaiBuzz));
    System.out.println("Woody : Andy = " + Arrays.equals(nilaiWoody, nilaiAndy));
  }
}
```
Output : 

```sh
Woody : Buzz = true
Woody : Andy = false
```

### `Arrays.toString()`

Mengembalikan sebuah representasi tipe data string dari sebuah array

```java
package main
import java.util.Arrays;

public class AksesArray{
  public static void main(String[] args){
    String[] buahBuahan = {"jeruk", "semangka", "melon", "pisang"};
    String stringBuahBuahan = Arrays.toString(buahBuahan);

    System.out.println(buahBuahan);
    System.out.println(stringBuahBuahan);
  }
}
```

Output:

```sh
[Ljava.lang.String;@1b28cdfa
[jeruk, semangka, melon, pisang]
```
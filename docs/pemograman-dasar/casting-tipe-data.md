---
sidebar_position: 7
slug: /casting
---

# A.7 Casting

## Casting Tipe Data

Casting adalah sebuah istilah untuk sebuah metode atau proses konversi suatu tipe data ke tipe data lainnya. Contohnya dari tipe data integer ke tipe data long dan sebaliknya.

Casting tipe data dalam java dibagi jadi 2 yaitu Manual Conversion dan Automatic Conversion

## Widening Type Casting

Widening type casting adalah proses konversi tipe data dengan syarat kedua tipe data yang ingin dikonversi compatible dan tipe data tujuan lebih besar daya tampungnya dari tipe data source.

Berikut merupakan alur yang dapat dilakukan operasi widening casting
byte -> short -> int -> long -> float -> double

```go
public class WideningCasting {
   public static void main(String args[]) {
       
    byte b = 16;
    short s = b;
    int i = s;
    long l = i;
    float f = l;
    double d = f;
    
    System.out.println("Ini tipe data byte : " + b);
    System.out.println("Ini tipe data short : "+ s);
    System.out.println("Ini tipe data integer : "+ i);
    System.out.println("Ini tipe data long : "+ l);
    System.out.println("Ini tipe data float : "+ f);
    System.out.println("Ini tipe data double : "+ d);
   }
}
```

Output:

```sh
Ini tipe data byte : 16
Ini tipe data short : 16
Ini tipe data integer : 16
Ini tipe data long : 16
Ini tipe data float : 16.0
Ini tipe data double : 16.0
```

## Narrowing Type Casting

Narrowing type casting adalah proses konversi tipe data dengan bantuan programmer untuk eksekusinya. Hal ini dikarenakan proses casting dilakukan ketika tipe data tujuan lebih rendah 
dari tipe data source.

Berikut merupakan alur yang dapat dilakukan operasi widening casting
double -> float -> long -> int -> short -> byte

```go
public class NarrowingCasting {
   public static void main(String args[]) {
       double d = 100000;
       float f = (float)d;
       long l = (long)f;
       int i = (int)l;
       short s = (short)i;
       byte b = (byte)s;
       
       System.out.println("Ini tipe data double : "+ d);   
	   System.out.println("Ini tipe data float : "+ f);
       System.out.println("Ini tipe data long : "+ l);
       System.out.println("Ini tipe data integer : "+ i);
       System.out.println("Ini tipe data short : "+ s);
       System.out.println("Ini tipe data byte : " + b);
   }
}
```

Output:

```sh
Ini tipe data double : 100000.0
Ini tipe data float : 100000.0
Ini tipe data long : 100000
Ini tipe data integer : 100000
Ini tipe data short : -31072
Ini tipe data byte : -96
```

Dapat dilihat dari output di atas. terjadi perubahan nilai pada tipe data short dan byte. Itu dikarenakan range dari short hanya 32.767 dan byte hanya 127 sedangkan nilai asli adalah 100000. 

## ASCII

ASCII (American Standard Code for Information Interchange) adalah sebuah standar baku yang digunakan untuk kode sebuah Character (char).

Informasi dari ASCII dapat digunakan untuk mengkonversi dari tipe data Character ke tipe data Numeric atau sebaliknya

```go
public class ASCII {
    public static void main(String args[]) {
        char[] chars = {'A', 'a', '!', '1', ' '};
        for(int i = 0; i < chars.length; i++){
            System.out.println(chars[i] + " = " + (int)chars[i]);
        }
        for(int i = 97; i < 110; i++){
            System.out.print((char)i + " ");
        }
    }
}
```

Output:

```sh
A = 65
a = 97
! = 33
1 = 49
  = 32
a b c d e f g h i j k l m 
```
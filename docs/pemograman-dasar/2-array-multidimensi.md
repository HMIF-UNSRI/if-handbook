---
sidebar_position: 12
slug: /array-multidimensi
---

# A.12 Array Multidimensi

Pada bagian sebelumnya, telah dijelaskan tentang Array 1 Dimensi. Bagian kali ini akan berfokus ke Array Multidimensi

## Apa itu Array Multidimensi
Array MultiDimensi merupakan sebuah konsep dimana setiap elemen dalam array mereference ke array lainnya. Dalam java, array multidimensi dapat dibuat dengan menambahkan kurung siku [] yang menandakan jumlah dimensi array tersebut.

## Struktur Array MultiDimensi

Struktur Array MultiDimensi menggunakan konsep yang sama dengan Array 1 Dimensi, hanya saja elemen dari dimensi arraynya mereference (diisi) dengan dimensi array 1 tingkat dibawahnya

```go
package main;
public class ArrayMultiDimensi{
    public static void main(String[] args){
        int[][] arrayDuaDimensi = new int[2][3];
        int[] arraySatuDimensiA = {1,2,3};
        int[] arraySatuDimensiB = {4,5,6};

        arrayDuaDimensi[0] = arraySatuDimensiA;
        arrayDuaDimensi[1] = arraySatuDimensiB;
    /*
        Sehingga Isi Dari arrayDuaDimensi
        [
             0 1 2
          0 [1,2,3]
          1 [4,5,6]
        ]
    */
        System.out.println("Index [0,0] : " + arrayDuaDimensi[0][0]);
        System.out.println("Index [1,2] : " + arrayDuaDimensi[1][2]);
    }
}
```

Output:
```sh
Index [0,0] : 1
Index [1,2] : 6
```

Seperti yang telah dijelaskan sebelumnya bahwa kita juga bisa membuat array 3 Dimensi hanya
dengan menambah ([]) di variabel yang ingin kita jadikan array 3 Dimensi

```go
package main;
public class ArrayMultiDimensi{
    public static void main(String[] args){

        int[] arraySatuDimensiA = {7,8,9};
        int[] arraySatuDimensiB = {10,11,12};

        int[][] arrayDuaDimensiA = {
            {1,2,3},
            {4,5,6}
        };

        int[][] arrayDuaDimensiB = {
            arraySatuDimensiA,
            arraySatuDimensiB,
        };

        int[][][] arrayTigaDimensi = {
            arrayDuaDimensiA,
            arrayDuaDimensiB,
        };

        System.out.println("Index [0,0,0] : " + arrayTigaDimensi[0][0][0]);
        System.out.println("Index [1,0,0] : " + arrayTigaDimensi[1][0][0]);
    }
}
```

Output:
```sh
Index [0,0,0] : 1
Index [1,0,0] : 7
```
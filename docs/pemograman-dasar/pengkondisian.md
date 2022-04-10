---
sidebar_position: 9
slug: /pengkondisian
---

# A.9 Pengkondisian

Pengkonsidisan digunakan untuk mengontrol alur program. Analoginya mirip seperti fungsi rambu lalu lintas di jalan raya. Kapan kendaraan diperbolehkan melaju dan kapan harus berhenti diatur oleh rambu tersebut. Seleksi kondisi pada program juga kurang lebih sama, kapan sebuah blok kode akan dieksekusi.

Yang dijadikan acuan oleh seleksi kondisi adalah nilai bertipe boolean, bisa berasal dari variabel, ataupun hasil operasi perbandingan. Nilai tersebut menentukan blok kode mana yang akan dieksekusi. Java memiliki 3 macam pengkondisian, yaitu : 

1. Pengkondisian if
2. Pengkondisian if else atau Ternary operator
3. Pengkondisian if else if atau Switch/Case

## IF

Dalam pembuatan program, ada saatnya butuh suatu pengkondisian, yakni jika sebuah kondisi terpenuhi, jalankan kode program ini, jika tidak jalankan kode program yang lain. Menggunakan bahasa Java, konsep tersebut dibuat menggunakan struktur IF.

Untuk menggunakan algoritma if bisa menggunakan syntax berikut :

```go
if(condition){
    // Kode program yang akan dijalankan jika condition bernilai true
}
```

Berikut Contoh implementasi untuk mengecek apakah suatu bilangan itu genap atau ganjil

```go
import java.util.Scanner;

public class Pengkondisian_If {
	public static void main(String args[]) {

		int a;
		Scanner input = new Scanner(System.in);

		System.out.print("Input sembarang angka: ");
		a = input.nextInt();

		if (a % 2 == 0) {
			System.out.println(a + " adalah angka genap");
		}
		if (a % 2 == 1) {
			System.out.println(a + " adalah angka ganjil");
		}

	}
}
```

Output : 

```sh
Input sembarang angka: 10
10 adalah angka genap
```

## IF-ELSE

Pada dasarnya, kondisi IF ELSE merupakan modifikasi tambahan dari pengkondisian IF. Blok kode program IF tetap akan dijalankan ketika kondisi true, namun sekarang terdapat tambahan bagian ELSE akan dijalankan ketika kondisi false.

Untuk menggunakan algoritma if bisa menggunakan syntax berikut :

```go
if(condition){
    // Kode program yang akan dijalankan jika condition bernilai true
}else{
    // Kode program yang akan dijalankan jika condition bernilai false
}
```
Sama seperti program sebelumnya, berikut merupakan program mengecek apakah suatu bilangan itu genap atau ganjil namun menggunakan algoritma IF-ELSE

```go
import java.util.Scanner;

public class Pengkondisian_IfElse {
	public static void main(String args[]) {
		int a;
		Scanner input = new Scanner(System.in);

		System.out.print("Input sembarang angka: ");
		a = input.nextInt();

		if (a % 2 == 0) {
			System.out.println(a + " adalah angka genap");
		} else {
			System.out.println(a + " adalah angka ganjil");
		}
	}
}
```

Output : 

```sh
Input sembarang angka: 6
6 adalah angka ganjil
```

## Ternary Operator

Ternary operator memiliki konsep yang sama seperti pengkondisian IF/ELSE, tapi dengan menggunakan ternary operator akan lebih mudah, karena mempersingkat baris kode program. 

Untuk menggunakan algoritma ternary operator bisa menggunakan syntax berikut :

```go
variablePenampung = kondisi ? expression1 : expression2;
```

variablePenampung akan menyimpan nilai expression1 jika kondisi bernilai true dan akan menyimpan nilai expression2 jika kondisi bernilai false

```go
public class Pengkondisian_TernaryOperator {
	public static void main(String args[]) {

		boolean suka = true;
		String jawaban;

		// menggunakan operator ternary
		jawaban = suka ? "iya" : "tidak";

		// menampilkan jawaban
		System.out.println(jawaban);
	}
}
```

Output : 

```sh
iya
```

## IF-ELSE IF

Pada dasarnya, kondisi IF ELSE IF adalah sebuah struktur logika program yang di dapat dengan cara menyambung beberapa perintah IF ELSE menjadi sebuah kesatuan.

Jika kondisi pertama tidak terpenuhi atau bernilai false, maka kode program akan lanjut ke kondisi IF di bawahnya. Jika ternyata tidak juga terpenuhi, akan lanjut lagi ke kondisi IF di bawahnya lagi, dst hingga blok ELSE terakhir atau terdapat kondisi IF yang menghasilkan nilai true.

Berikut format dasar penulisan kondisi IF ELSE IF dalam bahasa Java:

```go
if (condition_1) {
	// Kode program yang dijalankan jika condition_1 berisi nilai True
} else if (condition_2) {
	// Kode program yang dijalankan jika condition_2 berisi nilai True
} else if (condition_3) { 
	// Kode program yang dijalankan jika condition_3 berisi nilai True 
} else  { 
	// Kode program yang dijalankan jika semua kondisi tidak terpenuhi
}
```
Berikut Implementasi dari algoritma IF-ELSE IF

Sebagai contoh pertama adalah kode program untuk menampilkan nilai. User diminta menginput sebuah huruf antara ‘A’ – ‘E’. Kemudian program akan menampilkan hasil yang berbeda-beda untuk setiap huruf, termasuk jika huruf tersebut di luar ‘A’ – ‘E’.

```go
import java.util.Scanner;

public class Pengkondisian_If_ElseIf {
  public static void main(String args[]){
     
    char nilai;
    Scanner input = new Scanner(System.in);
     
    System.out.print("Input Nilai Anda (A - E): ");
    nilai = input.next().charAt(0);
     
    if (nilai == 'A' ) {
      System.out.println("Pertahankan!");
    }
    else if (nilai == 'B' ) {
      System.out.println("Harus lebih baik lagi");
    }
    else if (nilai == 'C' ) {
      System.out.println("Perbanyak belajar");
    }
    else if (nilai == 'D' ) {
      System.out.println("Jangan keseringan main");
    }
    else if (nilai == 'E' ) {
      System.out.println("Kebanyakan bolos...");
    }
    else {
      System.out.println("Maaf, format nilai tidak sesuai");
    }
    
  }
}
```

Output:

```sh
Input Nilai Anda (A - E): B
Harus lebih baik lagi
```

## Switch-Case

Kondisi SWITCH CASE adalah pengkondisian kode program dimana akan membandingkan isi sebuah variabel dengan beberapa nilai. Jika proses perbandingan tersebut menghasilkan true, maka block kode program akan di proses.

Kondisi SWITCH CASE terdiri dari 2 bagian, yakni perintah SWITCH dimana terdapat nama variabel yang akan diperiksa, serta 1 atau lebih perintah CASE untuk setiap nilai yang akan diperiksa.

Berikut format dasar penulisan kondisi SWITCH CASE dalam bahasa Java:

```go
switch (nama_variabel) {
	case 'nilai_1':
		// Kode program yang dijalankan jika nama_variabel == nilai_1
	break;
	case 'nilai_2':
		// Kode program yang dijalankan jika nama_variabel == nilai_2
	    break;
	case 'nilai_3':
		// Kode program yang dijalankan jika nama_variabel == nilai_3
	    break;
	...
	...
	default:
		// Kode program yang dijalankan jika tidak ada kondisi yang terpenuhi
}

```
Sama seperti program sebelumnya, program dimana akan membandingkan isi sebuah variabel dengan beberapa nilai namun menggunakan algoritma SwitchCase

```go
import java.util.Scanner;

public class SwitchCase {
	public static void main(String args[]) {

		char nilai;
		Scanner input = new Scanner(System.in);

		System.out.print("Input Nilai Anda (A - E): ");
		nilai = input.next().charAt(0);

		switch (nilai) {
		case 'A':
			System.out.println("Pertahankan!");
			break;
		case 'B':
			System.out.println("Harus lebih baik lagi");
			break;
		case 'C':
			System.out.println("Perbanyak belajar");
			break;
		case 'D':
			System.out.println("Jangan keseringan main");
			break;
		case 'E':
			System.out.println("Kebanyakan bolos...");
			break;
		default:
			System.out.println("Maaf, format nilai tidak sesuai");
		}

	}
}
```
Output : 

```sh
Input Nilai Anda (A - E): C
Perbanyak belajar
```

## Nested IF

 
Selanjutnya adalah pengkondisian yang ada di dalam pengkondisian (pengkondisian bersarang).Jadi, Pengkondisian bisa dibuat di dalam pengkondisian. Kadang teknik ini disebut juga nested if.

Contoh kasus:
Misalnya ada model bisinis seperti ini di sebuah toko. Ketika orang membayar di kasir, biasanya ditanya ada kartu member untuk mendapatkan diskon dan sebagainya.

```go
import java.util.Scanner;

public class Nested_If {
	public static void main(String[] args) {
		// deklarasi variabel dan Scanner
		int belanjaan, diskon, bayar;
		String kartu;
		Scanner scan = new Scanner(System.in);

		// mengambil input
		System.out.print("Apakah ada kartu member: ");
		kartu = scan.nextLine();
		System.out.print("Total belanjaan: ");
		belanjaan = scan.nextInt();

		// proses
		if (kartu.equalsIgnoreCase("ya")) {
			if (belanjaan > 500000) {
				diskon = 50000;
			} else if (belanjaan > 100000) {
				diskon = 15000;
			} else {
				diskon = 0;
			}
		} else {
			if (belanjaan > 100000) {
				diskon = 5000;
			} else {
				diskon = 0;
			}
		}

		// total yang harus dibayar
		bayar = belanjaan - diskon;

		// output
		System.out.println("Total Bayar: Rp " + bayar);
	}
}
```

Output : 

```sh
Apakah ada kartu member: ya
Total belanjaan: 350000
Total Bayar: Rp 335000
```


<h1 id="belajar-javascript" align="center">
	Belajar Javascript
	<img src="https://cdn.rawgit.com/gilbarbara/logos/a7e2b452/logos/javascript.svg" align="right" width="70" style="border-radius: 10%">
</h1>

<br>

<p align="center" style="padding-bottom: 2.5em; border-bottom: 1px solid #ddd">
	Repository ini berisi kumpulan materi yang membahas dasar programming javascript. Dengan adanya repository ini semua member ataupun non-member bisa berkonstribusi untuk menambahkan atau mengoreksi semua isi dalam artikel ini.
</p>

<p align="center" style="padding: 1em 0 .5em">
	<a href="#apa-itu-javascript">Apa itu javascript?</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
	<a href="#konten-daftar-isi">Konten (Daftar Isi)</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
	<a href="#">Cara Berkontribusi</a>
</p>

---

## Apa itu Javascript?

Javascript adalah salah satu bahasa pemrograman komputer yang pada awalnya diimplementasikan sebagai bagian dari web browser atau juga biasa disebut sebagai client-side script yang mana mampu berinteraksi dengan pengguna, memanipulasi content dokumen HTML, dan seterusnya. Belakangan javascript digunakan untuk server, pengembangan dalam dunia game, aplikasi real-time dan aplikasi desktop.

### ECMAScript

Javascript sendiri menerapkan standar [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript). [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) ini adalah standar bahasa script yang banyak dipakai oleh bahasa pemrograman yang ditujukan untuk pembuatan aplikasi yang berjalan di browser. Selain __Javascript__, __ECMAScript__ juga digunakan oleh *__ActionScript__*, *__QML__*, dsb.

Saat ini, versi ECMAScript yang sudah diterapkan adalah versi 6 atau juga disebut (__ES2015/ECMAScript 2015__). Beberapa javascript engine dan web browser (peramban) ternama seperti firefox, google chrome telah [mengimplementasikan ES2015](https://en.wikipedia.org/wiki/ECMAScript#Implementations) baik sebagai __front-end__ application maupun __back-end__ application pada sisi server ([Node.js](https://nodejs.org)).


## Konten (Daftar isi)

- [Syntax](#syntax)
- [Comment (Komentar)](#syntax)
- [Variable](#variable)
	- [var, let, const](#var-let-const)
- [Scope](#scope)
- [Booleans](#)
- [Numbers](#)
- [Strings](#)
- [Statements](#)
- [Functions](#functions)
- [Exception handling](#)
- [Strict mode](#)
- [Variable scoping dan closures](#)
- [Objects dan inheritance](#)
- [Arrays](#)
- [Regular expressions](#)
- [Math](#)

---

## Syntax

Contoh sederhana

```javascript
console.log('Hallo, Indonesia!');
//=> 'Hallo, Indonesia!'
```

## Comment (Komentar)

```javascript
// Komentar dalam satu baris
console.log('komentar di atas tidak di eksekusi');

/*
Membuat komentar untuk beberapa baris
atau juga disebut multiline.
*/
console.log('komentar diatas juga tidak akan di eksekusi');
```

## Variable dan assignment

Dalam javascript semua `variable` harus dideklarasikan dengan menggunakan syntax-keyword `var`, `let`, atau `const` lalu diikuti dengan nama variable. Setelah mendefinikasi `variable` kita dapat memberikan nilai atau tidak untuk variable tersebut, contoh:

```javascript
var x; // Mendefinisikan variable x tanpa nilai.
var y = 10; // Mendefinisikan variable y dengan nilai default 10
```

Karena javascript itu adalah bahasa pemrograman yang dinamis, deklarasi variable juga bisa dilakukan tanpa mengetikkan keyword `var` berulang ulang, contoh :

```javascript
var a, b = 10, c = 20;
```

Semua statement dalam javascript sebaiknya diakhiri menggunakan semicolon `;` (titik koma) untuk menghindari error.

Dalam sebuah dokumen HTML jika variable dideklarasikan diluar `function` tanpa menyertakan tipe / jenis keywordnya (`VariableDeclaration`), maka variable tersebut didefinisikan sebagai `global` variable oleh web browser, artinya variable tersebut menjadi sebuah `object` dari `window` contoh :

```javascript
idjs = "String";

function renderString() {
	return window.idjs;
}
```

### var, let, const

Dalam penulisan variable, javascript memiliki 3 tipe keyword deklarasi.

| Tipe    | Manipulasi   | Global Akses  |
| ------- | :----------: | :-----------: |
| `var`   | ✔            | ✔            |
| `let`   | ✔            | ✘            |
| `const` | ✘            | ✘            |

#### var

Pada keyword `var` kita dapat mendeklarasikan `variable` dengan memberikan nilai ataupun tanpa memberikan nilai secara default. Pada keyword ini, nilai dari variable dapat kita ubah pada saat kapapun jika diperlukan.

contoh :

```javascript
var memberAktif = false;
console.log(memberAktif);
//=> false

// fungsi aktivasi data member menjadi aktif pada kondisi tertentu
function aktivasiMember() {
	memberAktif = true;
}

// eksekusi fungsi aktivasi member
aktivasiMember();
console.log(memberAktif);
//=> true
```

Setelah kita membuat `script` seperti diatas dan menjalankan pada web browser, maka kita akan melihat perubahan nilai pada variable `memberAktif` yang sebelumnya bernilai `false` menjadi `true` setelah kita mengeksekusi fungsi `aktivasiMember();`. Istilah ini biasanya disebut juga dengan perubahan nilai `state` dari suatu variable.


#### let

Keyword `let` memiliki pendeketan yang tidak jauh berbeda dengan `var`, tetapi cukup kontras pada sisi implementasinya. Mari kita lihat pada contoh `script` berikut.

```javascript
var nama = 'nama komunitas';

function testVar() {
	var nama = 'idjs';
	console.log(nama);
	//=> 'idjs'

	console.log(this.nama);
	//=> 'nama komunitas'
}

// Menggunakan let
let githubUrl = 'link github';

function testLet() {
	githubUrl = 'https://github.com/idjs';
	console.log(githubUrl);
	//=> 'https://github.com/idjs'

	console.log(this.githubUrl);
	//=> undefined
}
```

Pada contoh `script` diatas, kita melihat keyword `this` yang merupakan [global](#global) `object` dari suatu `scope`, untuk lebih lengkapnya dibahas pada materi tentang [scope](#scope).

Dapat kita lihat perbedaan implementasi `var` dan `let` berdasarkan `script` yang telah kita buat. Nilai dari kedua `variable` dapat dimanipulasi tetapi `let` tidak mendapatkan hak untuk mengakses melalui jalur [global](#global) `object`.


#### const

Seperti pada tabel diatas, nilai pada tipe variable ini tidak dapat diubah. Simak contoh ini, dan bagaimana `const` bekerja.

```javascript
const namaBulanPertama = 'January';

namaBulanPertama = 'januari';
//=> TypeError: Assignment to constant variable.
```

Jika kita mencoba mengubah nilai yang ada pada jenis variable `const`, maka kita akan mendapatkan pesan `TypeError` pada layar `console` sebab nilai dari konstanta (baik dalam index) dan jenis datanya tidak dapat diubah.


## Booleans

## Numbers

## Strings

## Statements

## Functions

## Exception handling

## Strict mode

## Variable scoping dan closures

## Objects dan inheritance

## Arrays

## Regular expressions

## Math

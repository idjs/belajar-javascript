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

```
var x; // Mendefinisikan variable x tanpa nilai.
var y = 10; // Mendefinisikan variable y dengan nilai default 10

// Komentar dalam satu baris

/*
Komentar multiline (banyak baris).
*/

// Fungsi dengan balikan string berupa kalimat
function idjs() {
  return "Ini adalah contoh fungsi sederhana";
}

// Mendifiniskan fungsi dalam variable, dalam dunia programming biasanya disebut dengan lambda
var idjs = function() {
  return "Halo alam semesta";
};
```

## Variable dan assignment

Dalam javascript semua variable harus dideklarasikan dengan menggunakan syntax-keyword "var" diikuti dengan nama variable, bisa diikuti atau tidak diikuti dengan nilai yang diberikan kepada variable, contoh:

```
var a;
var b = 10;
```

Karena javascript itu adalah bahasa pemrograman yang dinamis, deklarasi variable juga bisa dilakukan tanpa mengetikkan keyword "var" berulang ulang, contoh :

```
var a, b = 10, c = 20;
```

Semua statement dalam javascript sebaiknya ditutup menggunakan semicolon (; / titik koma) untuk menghindari error.

Dalam sebuah dokumen HTML jika variable dideklarasikan diluar function tanpa menyertakan keyword var, maka variable tersebut didefinisikan sebagai global variable oleh web browser, artinya variable tersebut menjadi sebuah ```object``` dari ```window``` contoh :

```
idjs = "String";

function renderString() {
  return window.idjs;
};
```

## Values

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

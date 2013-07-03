Belajar Javascript
==================

Repository ini berisi ebook kumpulan berbagai artikel yang membahas dasar programming javascript. Dengan adanya repository ini semua member ataupun non-member bisa berkonstribusi untuk menambahkan atau mengoreksi semua isi dalam artikel ini.

Table of contents (Daftar isi)

1.	Pengenalan
2.	Syntax
3.	Variable dan assignment
4.	Values
5.	Booleans
6.	Numbers
7.	Strings
8.	Statements
9.	Functions
10.	Exception handling
11.	Strict mode
12.	Variable scoping dan closures
13.	Objects dan inheritance
14.	Arrays
15.	Regular expressions
16.	Math

## Pengenalan - Apa itu Javascript?

Javascript adalah salah satu bahasa pemrograman komputer yang pada awalnya diimplementasikan sebagai bagian dari web browser atau juga biasa disebut sebagai client-side script yang mana mampu berinteraksi dengan pengguna, memanipulasi content dokumen HTML, dan seterusnya. Belakangan javascript digunakan untuk server, pengembangan dalam dunia game, aplikasi real-time dan aplikasi desktop.

Javascript juga biasa dikenal dengan ECMAScript yang merupakan bagian utama dari web browser modern.

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

# Resummary 3 weeks
## JS-INTERMEDIATE ARRAY
### APA ITU ARRAY?**
- ``` Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array juga dapat menyimpan tipe data String, Number, Boolean, dan lainnya.``` 
### Array Iteration**
```
Array Iteration adalah Salah satunya topik iteration atau perulangan pada array. Perulangan sangat diperlukan untuk memudahkan dalam mengakses setiap elemen pada array. 
```
- *Namun array memiliki built-in method atau method bawaan sendiri yang dapat kita gunakan untuk melakukan perulangan. Berikut kelebihan built-in method yang akan dipelajari :*

1. Kode lebih mudah dibaca.
2. Mengurangi kesalahan ketika menggunakan banyak tanda operator seperti pada perulangan konvensional.
3. Menjaga variabel yang dimiliki tetap pada blok kodenya.

1. .forEach() 
```
struktur kode seperti di bawah ini:

array.forEach((value, index, array) => {
// kode program
})
```

2. .Map() 
```
arr.map((value, index, array) => {
  // kode program
});
```
3. .reduce()
```
Struktur kode dari .reduce():

arr.reduce((total, value, index, array) => {
  // kode program
}, initialValue);
```
4. .filter()
```
Struktur kode dari .filter():

arr.filter((value, index, array) => {
  // kode program
});
```
5. .indexOf()
``` 
Struktur kode dari .indexOf():

arr.indexOf(value, startIndex);
```
6. .lastIndexOf()
```
Struktur kode dari .lastIndexOf():

arr.lastIndexOf(value, startIndex);
```
7. .find()
```
Struktur kode dari .find():

arr.find((value, index, array) => {
  // kode program
});
```
8. .findIndex()
```
Struktur kode dari .findIndex():

arr.findIndex((value, index, array) => {
  // kode program
});
```
9. .includes()
```
Struktur kode dari .includes():

array.includes("--data yang kita cari--");
```

### Apa itu array multidimensi?

- ```Array multidimensi sama halnya seperti array satu dimensi, namun yang membedakan adalah array multidimensi memiliki data array di dalamnya. Mudahnya ada array di dalam array.```

- **Mengapa ada array di dalam array?**
- ```ini karena array pada JavaScript dapat menyimpan berbagai macam tipe data termasuk array itu sendiri.```
 
- **Mengapa menggunakan array multidimensi?**
- ```ketika kita ingin menambahkan satu data lagi yaitu contohnya ketika kamu menyimpan banyak nama buah pada satu variabel array. ketika km ingin menambahkan data lagi pada saat itulah km bisa menggunakan array multidimensi ini. contoh data yg akan di tambahkan semisal jumlah buah yang terjual atau mungkin harga dari buah tersebut.```

- **Membuat Array Multidimensi**
- kita dapat mendeklarasikan menggunakan array literal seperti berikut ini:

``` 
let namaArray = [
  [elemen1, elemen2],
  [elemen3, elemen4],
  [elemen5, elemen6],
];
```
- Contoh menyimpan data dengan array multidimensi:

```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

console.log(inventory);
/* Output:
[
 ["Kaos Polos", 21],
 ["Jaket Hoodie", 13],
 ["Topi", 7],
]
*/
```
- *Berdasarkan contoh di atas, variabel inventory merupakan variabel yang menyimpan data array. Di dalamnya, terdapat array lainnya yang menampung informasi terkait barang yang disimpan. Dengan begitu, variabel inventory dapat disebut dengan array multidimensi.*

**Bagaimana cara mengakses Array Multidimensi?**
- cara mengaksesnya sama seperti kita mengakses array satu dimensi karna, Kita hanya perlu mengakses nomor index untuk mengakses elemen yang terdapat pada array multidimensi.
- **CONTOH:**

```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

console.log(inventory[0][0]); // Output: Kaos Polos
console.log(inventory[2][0]); // Output: Topi
console.log(inventory[1][1]); // Output: 13
Sama seperti array satu dimensi, array multidimensi juga dapat menggunakan property dan method bawaan dari tipe data array.
```
**Looping pada Array Multidimensi**

- Di bawah ini merupakan contoh penggunaan beberapa perulangan yang dapat digunakan ketika kamu ingin mengakses data pada masing-masing elemen:

- Menggunakan .for():
```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

for (let i = 0; i < inventory.length; i++) {
  for (let j = 0; j < inventory[i].length; j++) {
    console.log(inventory[i][j]);
  }
}

// Output:
// Kaos Polos
// 21
// Jaket Hoodie
// 13
// Topi
// 7
```
- Menggunakan .forEach():
```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

inventory.forEach((baris) => {
  baris.forEach((kolom) => {
    console.log(kolom);
  });
});

// Output:
// Kaos Polos
// 21
// Jaket Hoodie
// 13
// Topi
// 7
```
- Menggunakan .map():
```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

inventory.map((baris) => {
  baris.map((kolom) => {
    console.log(kolom);
  });
});

// Output:
// Kaos Polos
// 21
// Jaket Hoodie
// 13
// Topi
// 7
```
**Menambahkan Data Array Multidimensi**
- Berikut adalah salah satu contoh yang dapat digunakan untuk menambah data ke dalam array:

- Menggunakan .for():
```
let inventory = [
  ["Kaos Polos", 21],
  ["Jaket Hoodie", 13],
  ["Topi", 7],
];

// total produk dikurangi data yg terjual
for (let i = 0; i < inventory.length; i++) {
  let stokTersisa = 100 - inventory[i][1];
  inventory[i].push(stokTersisa);
  ```
  ### Apa itu rekursif?

- Rekursif adalah *suatu teknik pemrograman yang menggunakan function atau fungsi. Sederhananya adalah fungsi yang memanggil fungsi tersebut atau dirinya sendiri, seolah-olah terjadi suatu perulangan. Proses pemanggilan inilah yang disebut sebagai recursion (rekursi) dan akan terus dilakukan sampai pada kondisi yang sudah ditentukan.*

**Kelebihan & Kekurangan rekursif.**
- Dengan menggunakan rekursif, memungkinkan kamu untuk dapat merancang suatu logika penyelesaian menjadi lebih baik dan mudah dibaca. Namun dari kelebihannya itu, rekursif menggunakan banyak memori sehingga membuat aplikasi menjadi lambat jika data yang diuji sangat banyak.

- Ada 3 hal yang perlu diperhatikan untuk memutuskan kapan menggunakan rekursif dan kapan menggunakan iteratif:

- *Jika fokus kamu adalah kecepatan pada aplikasi dan menghemat memori, kamu harus menggunakan iteratif.
Jika data yang diuji tidak banyak, kamu dapat menggunakan rekursif.
Beberapa algoritma secara natural lebih cocok menggunakan rekursif*.

**Membuat Rekursif**
- Algoritma rekursif mempunyai 2 komponen utama, yaitu:

1. Base Case
Kasus dasar untuk menyelesaikan permasalahan. Base case akan dikunjungi jika rekursi berakhir (kondisi untuk berhenti terpenuhi), serta mengembalikan nilai tanpa melakukan rekursi kembali.

2. Recursion Call
Permasalahan yang ada tentunya akan diperkecil dengan melakukan pemanggilan function itu sendiri (recursion call). Permasalahan dapat diperkecil dengan mengurangi atau memecahkan data input pada setiap pemanggilannya hingga mencapai base case.

**Struktur dasar function rekursif adalah sebagai berikut:**
```
function namaFuncRekursif() {
  if (condition) {
    // Base case
  } else {
    // Recursion call
    namaFuncRekursif();
  }
}
```
### Apa itu Regex
- Regular Expression atau disebut juga Regex / Regexp adalah deretan karakter spesial yang menggambarkan pattern atau pola untuk pencarian teks pada sebuah string atau document.

**Kapan sih kita harus menggunakan regex?**

- Validasi input dari sebuah form
- Mencari keyword tertentu pada email atau halaman website
- Mencari IP address dalam kisaran tertentu

**Cara membuat pola regex**
- Ada dua cara untuk membuat regex, kita bisa menggunakan regex literal dengan menuliskan pola yang ingin dicari di antara dua slash / seperti ini:

 ```
 const namaVariable = /pola/;
 ```
- atau bisa juga menggunakan fungsi RegExp seperti ini:

```
const namaVariable = new RegExp("pola");
```
Lalu apa perbedannya? Dengan menggunakan regex literal, kita dapat meningkatkan performa karena akan selalu tetap constant, sedangkan fungsi RegExp bisa digunakan untuk pola yg dinamis, misalnya pola didapat dari user input atau dari hasil manipulasi string.

**Method pada Regex**

| Method | pengertian |
| ----------- | ----------- | 
| .exec() | Digunakan untuk mencari string yang kita inginkan pada pola regex yang tersedia dengan mengembalikan nilai array atau null. |
| .test() | Digunakan untuk string matching dari pencarian teks pada pola regex yang tersedia dengan mengembalikan nilai boolean (true/false). |

### apa itu module

- Module adalah sebuah cara bagi JavaScript untuk mengisolasi kode dari suatu file ke dalam sebuah file terpisah. Sehingga kode tersebut dapat digunakan berulang kali dengan cara di-export dari suatu file dan di-import ke file yang lainnya. Kita dapat melakukan export kode apapun pada JavaScript seperti string, object, array, number, hingga function.
- cara membuat module pada lokal directori:
``` 
<script type="module" src="index.js"></script>
```
**Export and Import**

> Module pada file JavaScript membutuhkan penghubung antar satu file dengan file yang lain. Untuk bisa menghubungkan file antar JavaScript kita bisa menggunakan export dan import sehingga memungkinkan untuk saling menggunakan kode antar module.

**Export**
Export digunakan untuk meng-export variabel pada file JavaScript. Variabel yang di_export_ dapat berisi data seperti string, object, array, hingga function.

Contoh dasar melakukan export pada variabel :
```
export let name = "Thoriq";
Kita tidak bisa langsung meng-export data tanpa disimpan ke dalam variabel terlebih dahulu seperti ini:

export 'Thoriq';
Kita juga bisa melakukan export pada objek JavaScript:

export let orang = {
  nama: "Thoriq",
  umur: 25,
  alamat: "Jl. Kemang Raya",
};
```
**Import**
- Import diibaratkan sebagai pasangan dari export. Jadi import digunakan untuk menggunakan variabel yang sudah di-export dari module lainnya. Contoh dasar melakukan import variabel :
```
import { data } from "./namaModul.js";
Contoh penggunaan dari import dengan menggunakan file export dari contoh di atas :

// index.js
import { name, orang, sayHello } from "./user.js";

// Menggunakan hasil import
console.log(name); // Output: Thoriq
console.log(orang); // Output: {nama: "Thoriq", umur: 25, alamat: "Jl. Kemang Raya"}
sayHello(orang.nama); // Output: Hello, Thoriq!
```
### OOP
- OOP adalah suatu paradigma atau konsep di dunia pemrograman yang berorientasikan pada objek. Biasanya objek memiliki 2 komponen, yaitu ciri-ciri dari objek tersebut (properti) dan kemampuan yang dapat dilakukan oleh objek tersebut (method).

- Contohnya pada dunia nyata terdapat objek makhluk hidup seperti manusia yang memiliki nama, umur, dan** jenis kelamin**. Manusia juga dapat melakukan aktifitas seperti tidur, belajar, bermain dan sebagainya.

**CLASS**
- Contoh pembuatan class Hewan dengan properti nama dan kaki dilengkapi dengan method .tidur():
```
class Hewan {
  constructor(nama, kaki) {
    this.nama = nama; // properti
    this.kaki = kaki; // properti
  }

  // Method
  tidur() {
    return `${this.nama} sedang tidur`;
  }
}
```
### WEB STROGE
- web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.
1. Cookies
- Apa itu cookies
> Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB)
2. Local Storage dan Session Storage
> Dengan memanfaatkan local storage dan session storage, kita dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web. 

### SYNCHRONOUS & ASYNCHRONOUS
**Apa itu synchronous?**

- Synchronous adalah saat kita mengeksekusi perintah satu persatu dan berurutan. Analoginya seperti kita sedang mengantri di kasir atau loket. Ketika ada 1 perintah masuk maka dia akan dieksekusi terlebih dahulu. Jika perintah belum selesai dan sudah ada perintah baru maka perintah kedua (yang baru) akan mengantri sampai perintah 1 selesai. Proses seperti ini disebut blocking dan membuat perintah kita tereksekusi dengan lambat.
```
Contoh :

console.log("antrian 1");
console.log("antrian 2");
console.log("antrian 3");

// output
// antrian 1
// antrian 2
// antrian 3
Kode di atas bersifat synchronous yaitu kode dijalankan baris per baris. Maka output kode di atas tereksekusi sesuai urutan perintahnya.
```
**Apa itu Asynchronous ?**
- Asynchronous adalah kebalikan dari synchronous.
- Ada beberapa cara untuk membuat proses asynchronous. Kami membatasi hanya memberikan 2 cara ini:

1. setTimeout(function, milliseconds) digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali.
2. setInterval(function, milliseconds) digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan.
> Contoh asynchronous menggunakan setTimeout():
```
setTimeout(() => {
  console.log("Cuci baju"); // proses asynchronous
}, 1000);
console.log("Menyapu");
console.log("Mengepel");
console.log("Memasak");

// 1000 ms = 1 second

// Output:
// Menyapu
// Mengepel
// Memasak
// Cuci baju
```
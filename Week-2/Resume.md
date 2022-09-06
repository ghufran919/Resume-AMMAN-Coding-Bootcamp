## **JavaScript Basic**
JavaScript adalah salah satu dari 3 bahasa yang harus dipelajari oleh semua pengembang web: 
- HTML untuk menentukan konten halaman web
- CSS untuk menentukan tata letak halaman web
- JavaScript untuk memprogram perilaku halaman web

## JavaScript Functions
_Functions_ sangat penting dan berguna dalam bahasa pemrograman apa pun karena membuat kode dapat digunakan kembali. _Functions_ adalah blok kode yang akan dijalankan hanya jika dipanggil. Jika kita memiliki beberapa baris kode yang perlu digunakan beberapa kali, kita dapat membuat fungsi termasuk baris kode berulang dan kemudian memanggil _functions_ tersebut.

    let panjang =100;
    let lebar = 50;
    function LuasPersegiPanjang(p,l) {
    return p * l;
    }
    console.log (LuasPersegiPanjang(p, l));
    
Diatas adalah contoh fungsi untuk menampilkan hasil dari luas persegi panjang.

JavaScript memiliki cakupan fungsi (_function scope_). Setiap fungsi membuat cakupan baru. Variabel yang didefinisikan di dalam fungsi tidak dapat diakses (_visible_) dari luar fungsi. Variabel yang dideklarasikan dengan _var_ , _let_ dan _const_ sangat mirip ketika dinyatakan di dalam fungsi.

## JavaScript Data Type Built in Prototype and Method
JavaScript adalah bahasa yang diketik secara longgar dan dinamis. Variabel dalam JavaScript tidak secara langsung terkait dengan jenis nilai tertentu, dan variabel apa pun dapat ditetapkan (dan ditetapkan kembali) nilai dari semua jenis:

 let foo = 42;    // foo is now a number
 foo     = 'bar'; // foo is now a string
 foo     = true;  // foo is now a boolean

Jenis-jenis data dalam JavaScript terdiri dari _objects_ dan _primitive values_
- _**Primitive values**_:

1. _Boolean type_
2. _Null type_
3. _Undefined type_
4. _Number type_
5. _BigInt type_
6. _String type_
7. _Symbol type_

- _**Objects**_

Setiap _function_ dan _objects_ dalam JavaScript memiliki properti bawaan, yang disebut _prototype_. _Prototype_ itu sendiri adalah objek, sehingga _prototype_ akan memiliki _prototype_ sendiri, membuat apa yang disebut rantai _prototype_. Rantai berakhir ketika kita mencapai _prototype_ yang memiliki _null_ untuk _prototype_ sendiri.

 function Person () { this.name = 'Ghufran', this. age = 22 } const person = new Person(); // 

## JavaScript Variable

Variabel digunakan untuk menyimpan nilai (name = "Ghufran") atau ekspresi (sum = x y). Sebelum menggunakan variabel, kita harus terlebih dahulu mendeklarasikannya menggunakan kata kunci var untuk mendeklarasikan variabel seperti ini: 

 var name; 

Untuk menetapkan nilai ke variabel baik saat mendeklarasikan variabel atau setelah mendeklarasikan variabel.

 var name = "Ghufran"; atau 
 
 var name; 
 name = "Ghufran"; 

## JavaScript Array

Array adalah objek yang dapat menyimpan koleksi item. Array menjadi sangat berguna ketika kita perlu menyimpan data dalam jumlah besar dengan jenis yang sama. Kita dapat mengakses item dalam array dengan merujuk ke _index number_-nya dan indeks elemen pertama array adalah nol. 

Untuk membuat array di JavaScript maka yang kita ketik adalah:

 var students = ["Ahmad", "Ghufran"]; 

Indeks "Ahmad" dan "Ghufran" masing-masing adalah 0 dan 1. Jika kita ingin menambahkan lebih banyak elemen ke array students, maka dapat melakukannya seperti ini:

 students[2] = "Akbar";

Objek Array memiliki banyak properti dan metode yang membantu pengembang untuk menangani array dengan mudah dan efisien. Kita bisa mendapatkan nilai properti dengan menentukan arrayname.property dan output metode dengan menentukan arrayname.method().

1. length property –> Untuk mengetahui jumlah elemen dalam array.
2. prototype property –> Untuk menambahkan properti dan metode baru.
3. reverse method –> Untuk membalikkan urutan item dalam array.
4. sort method –> Untuk mengurutkan item dalam array.
5. pop method –> Untuk menghapus item terakhir dari array.
6. shift method –> Untuk menghapus item pertama dari array. 
7. push method –> Untuk menambahkan nilai sebagai item terakhir.

## For, While dan Do While Loop dalam JavaScript
Loop berguna ketika kita harus mengeksekusi baris kode yang sama berulang kali, untuk beberapa kali atau dengan kondisi tertentu.

Ada beberapa jenis _loop_ yakni:
- _for loop_ mengeksekusi blok kode selama kondisi tertentu benar dengan mengambil tiga argumen: _initialization, condition,_ dan _increment_. Ekspresi kondisi dievaluasi pada setiap _loop_. _Loop_ terus berjalan jika ekspresi menghasilkan _true_ atau benar.
- _while loop_ membuat _loop_ yang mengeksekusi pernyataan tertentu selama kondisi pengujian dievaluasi ke _true_. Kondisi ini dievaluasi sebelum melaksanakan pernyataan.
- _do … while loop_ membuat _loop_ yang mengeksekusi pernyataan tertentu sampai kondisi pengujian mengevaluasi ke _false_. Kondisi ini dievaluasi setelah mengeksekusi pernyataan, menghasilkan pernyataan yang ditentukan yang dijalankan setidaknya sekali.

## Conditional Statement
_Conditional statement_ digunakan untuk memutuskan aliran eksekusi berdasarkan kondisi yang berbeda. Jika suatu kondisi benar, kita dapat melakukan satu tindakan dan jika kondisinya salah, kita dapat melakukan tindakan lain.

Ada beberapa jenis _conditional statement_ seperti:
1.	_If statement_
2.	_If…Else statement_
3.	_If…Else If…Else statement_

## JavaScript DOM Manipulation
Dalam pengembangan website, DOM adalah singkatan dari _Document Object Model_. Ini adalah antarmuka pemrograman yang memungkinkan kita untuk membuat, mengubah, atau menghapus elemen dari dokumen situs web. Manipulasi DOM adalah ketika kita menggunakan JavaScript untuk menambah, menghapus, dan memodifikasi elemen situs web. Hal ini sangat umum dalam pengembangan web.



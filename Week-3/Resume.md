## Git vs. GitHub
Git adalah versi sistem kontrol yang memungkinkan kita mengelola dan melacak riwayat kode sumber yang kita miliki. GitHub adalah layanan hosting berbasis cloud yang memungkinkan kita mengelola repositori Git. Jika kita memiliki proyek sumber terbuka yang menggunakan Git, maka GitHub dirancang untuk membantu kita mengelolanya dengan lebih baik.

Alur kerja Git adalah rekomendasi tentang cara menggunakan Git untuk menyelesaikan pekerjaan dengan cara yang konsisten dan produktif. Alur kerja Git mendorong pengembang dan tim untuk memanfaatkan Git secara efektif dan konsisten.

Alur-alur yang dapat dilakukan seperti:

- Alur kerja Git terpusat memungkinkan semua anggota tim untuk membuat perubahan langsung ke cabang utama, dengan setiap perubahan dicatat dalam riwayat yang sedang berjalan. Alur kerja terpusat melibatkan setiap kontributor yang berkomitmen pada cabang utama tanpa menggunakan cabang lain.
- Alu kerja bercabang memungkinkan pekerjaan lebih efisien dengan adanya _branch_ sebelum melakukan perubahan ke cabang utama sehingga meminimalisir kesalahan pekerjaan akibat miskomunikasi.

## **JavaScript Intermediate**

## Array dan Multidimensional Array
Kita dapat membuat _multidimensional array_ dengan mendefinisikan array elemen, di mana setiap elemen juga merupakan array lain. Untuk alasan ini, kita dapat mengatakan bahwa _multidimensional array_ JavaScript adalah array yang berisikan array lain.

**Contoh**

    const data = [[1, 2, 3], [1, 3, 4], [4, 5, 6]];
 



## Object
Dalam JavaScript, objek adalah entitas tunggal, dengan properti dan tipe. Objek adalah variabel. Variabel JavaScript dapat berisi nilai tunggal juga dapat berisi banyak nilai. Objek juga merupakan variabel, tetapi objek dapat mengandung banyak nilai. Nilai objek ditulis sebagai nama : nilai secara berpasangan (nama dan nilai dipisahkan oleh titik dua).

**Contoh**

    let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};


## Recursive
Fungsi rekursif adalah fungsi yang memanggil dirinya sendiri sampai berakhir. Metode ini disebut rekursi. 

**Contoh**

    countDown(fromNumber) {
    console.log(fromNumber);

    let nextNumber = fromNumber - 1;

    if (nextNumber > 0) {
        countDown(nextNumber);
        }
    }
    countDown(3);


## Regular Expression (RegEx)
_Regular expression_ adalah pola yang digunakan untuk mencocokkan kombinasi karakter dalam _string_. Dalam JavaScript, _regular expression_ juga merupakan _object_.

## Object Oriented Programming (OOP) and Modules
Modul dalam JavaScript hanyalah file yang berisi kode terkait. Di JavaScript, kita menggunakan kata kunci impor dan ekspor untuk berbagi dan menerima fungsionalitas masing- masing di berbagai modul. Kata kunci ekspor digunakan untuk membuat variabel, _function_, _class_ atau _object_ dapat diakses oleh modul lain.

 _Object oriented programming_ adalah segala hal tentang pemodelan sistem sebagai kumpulan objek, di mana setiap objek mewakili beberapa aspek tertentu dari sistem. Objek berisi fungsi (atau metode) dan data. 
 
 Terdapat tiga konsep utama dari OOP yakni:
1. _classes and instances_;
2. _inheritance_; 
3. _encapsulation_.

## Web Storage
Web Storage API menyediakan mekanisme di mana browser dapat menyimpan _key/value_ dengan cara yang jauh lebih intuitif daripada menggunakan _cookie_. 

Mekanisme dalam Web Storage adalah sebagai berikut: 
- sessionStorage mempertahankan area penyimpanan terpisah untuk setiap asal tertentu yang tersedia selama sesi halaman (selama browser terbuka, termasuk pemuatan ulang dan pemulihan halaman) serta menyimpan data hanya untuk sesi, artinya data disimpan hingga browser (atau tab) ditutup. Data tidak pernah ditransfer ke server. Batas penyimpanan lebih besar dari cookie (paling banyak 5MB).
- localStorage melakukan hal yang sama, tetapi tetap ada bahkan ketika browser ditutup dan dibuka kembali. Menyimpan data tanpa tanggal kedaluwarsa, dan hanya dihapus melalui JavaScript, atau membersihkan cache Browser.

Mekanisme ini tersedia melalui properti Window.sessionStorage dan Window.localStorage

## Asynchronous
_Asynchronous programming_ adalah teknik yang memungkinkan program untuk memulai tugas yang berpotensi berjalan lama dan masih dapat responsif terhadap peristiwa lain saat tugas itu berjalan, daripada harus menunggu sampai tugas itu selesai. Setelah tugas itu selesai, program disajikan dengan hasilnya.

_Event handlers_ merupakan bentuk pemrograman asinkron. Kita menyediakan fungsi (_event handlers_) yang akan dipanggil, tidak segera, tetapi setiap kali peristiwa itu terjadi. 

_Fetch API_ memungkinkan untuk meminta sumber daya secara asinkron. Gunakan metode fetch() untuk mengembalikan _promise_ yang diselesaikan ke dalam _Response object_. Untuk mendapatkan data aktual, kita dapat memanggil salah satu metode _Response object_ misalnya, text() atau json(). Metode-metode ini diselesaikan ke dalam data aktual.
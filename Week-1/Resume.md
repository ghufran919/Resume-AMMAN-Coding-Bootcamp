## Unix Command-line
_Unix command line_ adalah _‘shell’_ atau _‘terminal’_ yang digunakan untuk menjalankan perintah dalam program atau mengeksekusi perintah dalam sistem. Beberapa perintah yang sering digunakan dalam melakukan operasi melalui ‘PowerShell’ seperti: 

1. ls, _command_ yang digunakan untuk menampilkan _list file_ yang berada dalam suatu directory; 
2. cd, _command_ yang digunakan untuk mengganti _directory_; 
3. touch, _command_ yang digunakan untuk membuat suatu _file_ baru menggunakan; 
4. mkdir, _command_ yang digunakan untuk membuat _folder_ baru; 
5. rm, _command_ yang digunakan untuk mengganti nama atau menghapus _file_; dsb.

## Git and GitHub
Git adalah tools untuk melacak setiap perubahan _file_ atau kode. Beberapa command yang digunakan dalam git diantaranya: 

1. git config --list melihat konfigurasi git kita; 
2. git init --menginstall git di _folder/directory_ kerja kita; 
3. git status --  mengecek status dari git kita, biasanya itu tentang file yang belum di add atau di commit, jika sudah aman harusnya message yang keluar _"nothing to commit, working tree clean"_; 
4. git add <nama file> --  menambahkan 1 file ke _staging area_ dan masih perlu _commit_; 
5. git add .-- menambahkan seluruh file yang belum di _add_ ke _staging area_ dan masih perlu _commit_; 
6. git commit -m "pesan yang mengdeskripsikan apa yang kita lakukan" meng acc , meng _commit_ tentang penambahan checkpoint; 
7. git log --  melihat _history_ / kumpulan _checkpoint_ (_commit_) yang telah kita buat; 
8. git revert <nomor commit> kembali ke _checkpoint_ tanpa menghapus commitan sesudahnya; 
9. git reset <nomor commit> -- kembali ke _checkpoint_ dengan menghapus commitan sesudahnya; 
10. git branch -- melihat kumpulan _branch_; 
11. git branch <nama branch yang di inginkan> --  membuat _branch_ baru; 
12. git checkout <nama branch> --  pindah ke _branch_ yang kita inginkan; 
13. git checkout -b <nama branch> --  membuat _branch_ baru dan langsung pindah ke _branch_ yang kita baru buat; 
14. git branch -d <nama branch> --  menghapus _branch_; 
15. git merge <nama target branch yang ingin kita tarik> --  menggabungkan kedua buah _branch_.

GitHub adalah sebuah platform khusus developer yang memberikan layanan berupa pengelolaan project hingga kolaborasi dalam pembuatan website maupun _software_ serta segala hal-hal yang menggunakan ‘coding’ di dalamnya.

Developer yang menggunakan Git dapat menggunakan _command-line tool_, yaitu pengubah kode dan dapat digabungkan menuju perangkat lokal. Sedangkan, GitHub menyediakan _interface_ grafis berbasis cloud sebagai tempat untuk melakukan seluruh tugas.

## Algorithm and Data Structure
Pada dasarnya fungsi utama dari algoritma adalah untuk memecahkan suatu masalah. Suatu algoritma pemrograman membawa keuntungan serta fungsi penting dalam aktivitas pembuatan program. Algoritma pada umumnya digunakan untuk membantu setiap orang yang ingin mengkonversikan sebuah permasalahan ke bahasa pemrograman.

Untuk merubah algoritma tersebut menjadi bahasa yang dapat mudah untuk diterapkan pada koding, dibutuhkan konversi dari algoritma menjadi _pseudocode_. Hal tersebut bertujuan untuk mendapatkan gambaran bagaimana alur dari program yang akan dibuat.

![Gambar](https://www.dicoding.com/blog/wp-content/uploads/2021/08/Contoh-pseudocode-ganjil-genap.png)

Disitu dapat kita lihat susunan dari _pseudocode_ yakni:

- Judul: Sesuai dengan namanya, bagian ini digunakan untuk menunjukan judul dari algoritma yang akan ditulis oleh programmer.

- Deklarasi: Deklarasi ini berisi keterangan seperti variabel atau konstanta yang digunakan dalam penulisan algoritma.

- Algoritma: Algoritma ini berisikan proses atau perintah atau langkah dari algoritma. Ia dapat diartikan sebagai inti dari pseudocode. Kamu dapat menuliskan segala proses pada bagian ini, seperti proses kondisional (_if/else_), perulangan (for), atau operasional (penjumlahan, pengurangan, dan sebagainya).

Adapun notasi yang digunakan untuk mengetahui proses yang terjadi antara lain:

- _INPUT_: Digunakan untuk menunjukan proses memasukan suatu isi variabel.

- _OUTPUT_: Digunakan untuk menunjukan proses keluaran yang terjadi.

- _WHILE_: Digunakan untuk sebuah perulangan yang memiliki iterasi awal.

- _FOR_: Digunakan untuk sebuah perulangan perhitungan iterasi.

- _REPEAT – UNTIL_: Digunakan untuk sebuah perulangan yang memiliki kondisi akhir.

- _IF – THEN – ELSE_: Digunakan untuk mengambil sebuah keputusan dari beberapa kondisi.

## HTML

HTML (_Hyper Text Markup Language_) adalah bahasa markup standar untuk membuat halaman Web. HTML menjelaskan struktur halaman Web serta terdiri dari serangkaian elemen-elemen yang kemudian memberi tahu browser cara menampilkan konten.

- Elemen dan Tag: HTML menggunakan tag dan elemen yang telah ditentukan sebelumnya yang memberi tahu browser cara menampilkan konten dengan benar.

- Struktur halaman HTML: Struktur dasar halaman HTML diletakkan di bawah ini. Ini berisi elemen blok bangunan penting (yaitu _i.e. doctype declaration, HTML, head, title,_ dan _body elements_) di mana semua halaman web dibuat.

![Gambar](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20220401160946/HTML-Basic-Format-768x534.png)

## CSS

CSS (_Cascading Style Sheets_) adalah bahasa _stylesheet_ yang digunakan untuk merancang halaman web agar menarik.Alasan menggunakan ini adalah untuk menyederhanakan proses pembuatan halaman web yang rapi. Ini memungkinkan untuk menerapkan gaya pada halaman web.

Ada tiga jenis CSS yang diberikan di bawah ini: 
- Inline: Inline CSS berisi properti CSS di bagian _body_ yang dilampirkan dengan elemen.
- Internal: Set aturan CSS harus berada di dalam file HTML di bagian head yaitu CSS tertanam di dalam file HTML.
- Eksternal: CSS eksternal berisi file CSS terpisah yang hanya berisi properti _style_ dengan bantuan atribut tag.
## Responsive Web Design
_Responsive web design_, juga disebut RWD, menjelaskan pendekatan desain web modern yang memungkinkan situs web dan halaman untuk merender (atau menampilkan) di semua perangkat dan ukuran layar dengan secara otomatis beradaptasi dengan layar, baik itu desktop, laptop, tablet, smartphone, dsb.

Desain web responsif bekerja melalui _Cascading Style Sheets_ (CSS), menggunakan berbagai pengaturan untuk melayani properti gaya yang berbeda tergantung pada ukuran layar, orientasi, resolusi, kemampuan warna, dan karakteristik lain dari perangkat pengguna.

- **Viewport**
Viewport adalah area jendela tempat konten web dapat dilihat. Ini seringkali tidak berukuran sama dengan halaman yang dirender, dalam hal ini browser menyediakan bilah gulir bagi pengguna untuk menggulir dan mengakses semua konten. 

Tag meta Viewport HTML  digunakan untuk membuat situs web responsif. Sehingga web page dapat menyesuaikan lebarnya sesuai dengan viewport.

- **CSS Relative Units**
Manfaat menggunakan unit relatif adalah bahwa dengan beberapa perencanaan yang cermat kita dapat membuatnya sehingga ukuran teks atau elemen lain berskala relatif terhadap semua yang lain di halaman.

Dalam satuan panjang relatif didefinisikan sebagai em, ex, ch dan rem. Ini adalah font-panjang relatif. Menggunakan nilai relatif berarti bahwa segala sesuatunya dapat meningkatkan dan menurunkan skala sesuai dengan beberapa nilai lainnya.

- **Media Query**
_Media query_ adalah adalah fungsionalitas HTML/CSS yang memungkinkan konten halaman Web untuk beradaptasi dengan jenis media tempat halaman tersebut dirender, seperti layar komputer atau layar ponsel atau tablet.

## Bootstrap
Bootstrap adalah kerangka kerja pengembangan _front-end open source_ gratis untuk pembuatan situs web dan aplikasi web. Dirancang untuk memungkinkan pengembangan responsif situs web _mobile-first_, Bootstrap menyediakan kumpulan sintaks untuk desain template.

**Layout and Grid System**

- _Containers_

_Container_ `b-container` adalah elemen tata letak paling dasar di Bootstrap.

1. _Fluid width container_-> Dengan menggunakan _fluid prop_ pada `b-container` akan membuat kontainer yang lebarnya selalu 100%, terlepas dari _breakpoint viewport_.
2. _Responsive fluid containers_ -> Memungkinkan kita untuk menentukan _container_ dengan _width _100% (_fluid_) sampai _breakpoint_ tertentu tercapai di mana `_max-width_` diterapkan.

- _Row_

_Row_ (`b-row` dan `b-form-row`) adalah pembungkus untuk `_columns_`. Setiap _columns_ memiliki `_horizontal padding_` untuk mengontrol ruang di antara mereka.

- _Columns_

`b-col` harus ditempatkan di dalam komponen `b-row`, atau elemen (seperti `div`) yang memiliki baris kelas yang diterapkan.

**Components**

Bootstrap dibundel dengan puluhan komponen yang dapat digunakan kembali untuk memberikan pengalaman pengguna dan interaksi pengguna yang baik di halaman web seperti _navigation bars, pop-ups, dropdowns, icons, buttons, pre-designed forms_ dan juga opsi ukuran untuk elemen DOM yang berbeda.
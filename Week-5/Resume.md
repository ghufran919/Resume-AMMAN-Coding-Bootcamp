## ReactJS Basic
ReactJS adalah pustaka JavaScript _open source_ untuk mengembangkan antarmuka pengguna (UI) dalam aplikasi web. 

## Pemasangan ReactJS

**Windows Version**

1. Instalasi [NodeJS](https://nodejs.org/en/download) 
2. Check Node melalui CMD dengan mengetik
> node --version
3. Check NPM melalui CMD dengan mengetik
> npm --version
4. Instalasi _React App Library_ melalui CMD dengan mengetik
> npm install -g create-react-app
2. Buka CMD ketik ('npx create-react-app nama-aplikasi')

## Inisialisasi Proyek dengan ReactJS
1. Buka Terminal atau Command Prompt (CMD)
2. Lakukan perintah pada terminal yang telah dibuka:

> npx create-react-app [name-project]

3. Install _React-router Library _

> npm install react-router@5.3.3

4. Inisialisasi proyek pada CMD dengan mengetik:

> npm start

Render akan dimulai pada https://localhost:3000/

## Fitur dalam ReactJS
- JSX

JSX adalah ekstensi untuk javascript. 

- DOM Virtual

ReactJS membuat DOM virtual. Hanya perubahan akhir DOM yang kemudian diperbarui di browser DOM. 

- _Components_

_Components_ berfungsi membantu memudahkan kode dengan membagi logika menjadi kode independen yang dapat digunakan kembali. Kita dapat menggunakan _components_ sebagai _functions_ dan _components_ sebagai _class_. _Components_ juga memiliki _state_, _props_.

Ada dua cara dalam membuat _component_, yakni dengan _function_ dan _class_. 

**_Stateful Components and Stateless Components_**

- _Stateful Components_ digunakan untuk membungkus kode dari stateless component dengan cakupan yang lebih banyak dan besar. _Components_ ini memiliki _state_ dan _props_ serta dibuat dengan class. Kelebihan dari _components_ jenis adalah memiliki _lifecycle_

      class Hello extends React.Component {
         render() {
            return(
                  <div>
                     Hello Statefull Component
                  </div>
            )
            }
         }

- _Stateless component_ atau _functional component_ adalah sebuah fungsi javascript yang hanya mengambil sebuah inputan, biasanya digunakan untuk membungkus _child components_ seperti _component table, button_ dsb. Components jenis ini tidak memiliki _state_ dan hanya memiliki _prop_. Pada umumnya _component_ ini di buat dengan _function_ karena _code_nya lebih ringkas

      const HelloComponent () => {
         return <p>Hello Functional Component</p>
      }

_**State dan Props**_

- _Props_: Singkatan dari _property_. Prop umumnya digunakan untuk komunikasi _data component_ dari _parent component_ ke _child component_.Prop bersifat _read-only_.

- _State_: Merupakan _data private_ sebuah _component_. Data ini hanya tersedia untuk _component_ tersebut dan tidak bisa di akses oleh _component_ lain. 

## Lifecyle dari Components

_Lifecyle_ dari _components_ dibagi menjadi tahap-tahap sebagai berikut:

- _Initialization_: Ini adalah tahap pertama dari _component life cycle_.
- _Mounting_: Pada fase ini, _Components_ dirender di dalam DOM. 

> componentDidMount(): Ini juga dipanggil ketika _component_ baru saja ditambahkan ke DOM.

> render(): Metode ini diterapkan pada semua _component_ yang dibuat. 

- _Update_: Dalam kondisi ini, DOM berinteraksi dengan pengguna dan diperbarui.

> shouldComponentUpdate() : Dipanggil ketika _component_ diperbarui.
> componentDidUpdate() : Dipanggil setelah _component_ diperbarui. 

- _UnMounting_: Status ini muncul ketika _component_ tidak diperlukan atau dihapus. 

> Component willUnmount(): Dipanggil ketika _Component_ dihapus atau dihancurkan.


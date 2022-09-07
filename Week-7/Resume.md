# ReactJS Lanjutan

# React-Router

React Router adalah pustaka standar untuk perutean di ReactJS. Ini memungkinkan navigasi di antara tampilan berbagai komponen dalam _React Application_, memungkinkan mengubah URL browser, dan menjaga UI tetap sinkron dengan URL.

### Pemasangan React-Router

Untuk menambahkan React-Router ke proyek yang sudah ada, hal pertama yang harus kita lakukan adalah menginstal dependensi dengan:

> $ npm install react-router-dom@6

Setelah proyek diatur dan React-Router diinstal, buka src/index.js di editor teks. Impor `BrowserRouter` dari `react-router-dom` kemudian bungkus aplikasi dalam `BrowserRouter`

**Contoh**

    import * as React from "react";
    import ReactDOM from "react-dom/client";
    import {BrowserRouter,Routes,Route,} from "react-router-dom";
    import "./index.css";
    import App from "./App";
    import reportWebVitals from "./reportWebVitals";

    const root = ReactDOM.createRoot(
    document.getElementById("root")
    );
    root.render(
    <React.StrictMode>
        <BrowserRouter>
            <Routers>
                <App/>
            </Routers>
        </BrowserRouter>
    </React.StrictMode>
    );

## Navigation

Gunakan `Link` untuk mengizinkan pengguna mengubah URL atau gunakan Navigasi untuk melakukannya sendiri.

**Contoh**

    import { Link } from "react-router-dom";

    function Home() {
    return (
        <div>
        <h1>Home</h1>
        <nav>
            <Link to="/">Home</Link> |{" "}
            <Link to="about">About</Link>
        </nav>
        </div>
    );
    }

## Nested Routers

Sebagian besar tata letak digabungkan ke segmen URL dan `React-router` mencakup ini sepenuhnya. Rute dapat bersarang di dalam satu sama lain, dan jalurnya juga akan bersarang.

**Contoh**

    function App() {
    return (
    <Routes>
        <Route path="invoices" element={<Invoices />}>
            <Route path=":invoiceId" element={<Invoice />} />
            <Route path="sent" element={<SentInvoices />} />
        </Route>
        </Routes>
    );
    }    

## **Browser Router**

BrowserRouter adalah antar muka yang direkomendasikan untuk menjalankan React Router di browser web. `BrowserRouter` menyimpan lokasi saat ini di bilah alamat browser menggunakan URL bersih dan bernavigasi menggunakan tumpukan riwayat bawaan browser.

`BrowserRouter window` default untuk menggunakan `defaultView` dokumen saat ini, tetapi juga dapat digunakan untuk melacak perubahan ke URL jendela lain.

**Contoh**

    import * as React from "react";
    import * as ReactDOM from "react-dom";
    import { BrowserRouter } from "react-router-dom";

    ReactDOM.render(
    <BrowserRouter>
        {/* The rest of your app goes here */}
    </BrowserRouter>,
    root
    );

## Hooks

_Hooks_ adalah tambahan baru di `React 16.8`. Hal ini memungkinkan kita untuk menggunakan status dan fitur React lainnya tanpa menulis _class_.

**Contoh**

    import React, { useState } from `react`;

    function Example() {
    // Declare a new state variable, which we`ll call "count"
    const [count, setCount] = useState(0);

    return (
        <div>
        <p>You clicked {count} times</p>
        <button onClick={() => setCount(count + 1)}>
            Click me
        </button>
        </div>
    );
    }

## State Management

State Management adalah pengaturan data agar data tersebut bisa digunakan secara berulang kali (_reusable_), bisa juga mengatur data-data yang dapat di share untuk _component_ yang lain. Redux terdiri dari beberapa tahap penyesuaian yakni:

- **Reducers**

_Reducer_ menentukan bagaimana status aplikasi berubah sebagai respons terhadap tindakan yang dikirim ke _store_.
- **Actions**

_Actions_ adalah objek JavaScript biasa yang mewakili muatan informasi yang mengirimkan data dari aplikasi ke _store_. _Actions_ memiliki jenis dan muatan opsional.

-  **Action Creators**

Di Redux, _action creators_ adalah fungsi yang mengembalikan objek _actions_. Bagian status yang baru dikembalikan kemudian disalurkan ke status aplikasi, yang kemudian disalurkan kembali ke aplikasi ReactJS, yang berujung pada semua komponen  dirender ulang. 

**Contoh**
         export function addTodo({ task }) {
         return {
             type: 'ADD_TODO',
             payload: {
             task,
             completed: false
             },
         }
         }

         // example returned value:
         // {
         //   type: 'ADD_TODO',
         //   todo: { task: '🛒 get some milk', completed: false },
         // }

- **Store**

_Store_ mengacu pada objek yang menyatukan tindakan dan reduksi yang memperbarui status sesuai dengan tindakan tersebut. Hanya ada satu _store_ dalam aplikasi 
Redux.

Kita membutuhkan Redux untuk membuat _store_. Kita menggunakan combineReducers untuk menggabungkan beberapa Redux menjadi satu. Untuk membuat _store_, kita mengimpor `combineReducers` dan meneruskannya ke `createStore`. Kemudian mengirimkan tindakan di aplikasi kami menggunakan _dispatch_ metode pengiriman _store_.

**Contoh**

    import { createStore } from 'redux';
    import todoReducer from `./reducers`;

    const store = createStore(todoReducer);

    store.dispatch(addTodo({ task: '📖 Read a book'}));
    store.dispatch(addTodo({ task: '🤔 Brainstorming idea' }));
    // ...
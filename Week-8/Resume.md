## React Context
_Context_ adalah API yang dibangun ke dalam _React_, mulai dari `React 16`. _React-context_ sangat bagus dalam meneruskan data yang dapat digunakan dalam _component_ apa pun di aplikasi. Jenis data ini meliputi: 

- Data tema (seperti mode gelap atau terang) 
- Data pengguna (pengguna yang saat ini diautentikasi) 
- Data khusus lokasi (seperti bahasa pengguna atau lokal) 

Data harus ditempatkan pada _React-context_ yang tidak perlu sering diperbarui. Karena _context_ tidak membuat _state management system_. Hal ini dibuat untuk membuat mengelola data lebih mudah.

Ada empat langkah untuk menggunakan konteks React: 
- Buat _Context_ menggunakan metode createContext.
- Ambil _Context_ yang dibuat dan bungkus _context provider_ dalam _component tree_
- Letakkan nilai apa pun pada _context provider_ menggunakan value prop. 
- Baca value itu dalam _component_ apa pun dengan menggunakan _context consumer_.

**Contoh**

    import React from 'react';
    export const UserContext = React.createContext();
    export default function App() {
     return (
        <UserContext.Provider value="Reed">
        <User />
        </UserContext.Provider>
    )
  }

    function User() {
    return (
    <UserContext.Consumer>
      {value => <h1>{value}</h1>} 
      {/* prints: Reed */}
    </UserContext.Consumer>
  )
}

## React Testing
_Testing_ adalah proses 3 langkah meliputi:
1. `Arrange`: aplikasi dalam keadaan asli tertentu.  
2. `Act`: Sesuatu terjadi (klik peristiwa, input, dll.).
3. `Assert`: Kemudian kita menegaskan, atau membuat hipotesis, tentang _state_ baru aplikasi. Tes akan lulus jika hipotesis benar dan gagal jika salah.

Tidak seperti _react component_, _testing_ tidak dijalankan di browser. `Jest` adalah _test runner_ dan _testing framework_ yang digunakan oleh React. 

**Contoh**

    describe('Testing sum', () => {
    function sum(a, b) {
       return a + b;
    }

    it('should equal 4',()=>{
       expect(sum(2,2)).toBe(4);
      })

    test('also should equal 4', () => {
        expect(sum(2,2)).toBe(4);
        }) 
    });

_Testing_ dilakukan untuk memastikan bahwa aplikasi akan berfungsi sebagaimana ditujukan untuk pengguna akhir. Memiliki _testing_ akan membuat aplikasi lebih kuat dan tidak terlalu rawan kesalahan. Hal ini adalah cara untuk memverifikasi bahwa kode melakukan apa yang diinginkan pengembang.

Ada beberapa jenis _testing_ yang dapat dilakukan seperti:
- `unit testing`: menguji bagian terisolasi dari aplikasi, biasanya dilakukan dalam kombinasi dengan _shallow rendering_. 

> contoh: komponen dirender dengan default props.

- `integration testing`: menguji apakah bagian yang berbeda berfungsi atau terintegrasi satu sama lain. Biasanya dilakukan dengan memasang atau merender _component_.

> contoh: menguji apakah _child component_ dapat memperbarui _context state_ dalam _parent_. 

- `end to end testing`: Biasanya tes multi langkah yang menggabungkan beberapa unit dan _integration test_ menjadi satu tes. Pengujian dilakukan di browser simulasi, mungkin ada atau mungkin tidak ada UI saat pengujian sedang berjalan. 

> contoh: menguji seluruh alur autentikasi. 

## React-testing-library
Untuk memasang `react-testing-library` kita dapat mengetik _command_ di CMD. 

> npm install @testing-library/react

**useState_

    import React from 'react';
    import ReactDOM from 'react-dom';
    import TestHook from '../test_hook.js';
    import {render, fireEvent, cleanup} from '@testing-library/react';
    import App from '../../../App'

        afterEach(cleanup)

        it('Text in state is changed when button clicked', () => {
         const { getByText } = render(<TestHook />);

        expect(getByText(/Initial/i).textContent).toBe("Initial State")

     fireEvent.click(getByText("State Change Button"))

        expect(getByText(/Initial/i).textContent).toBe("Initial State Changed")
     })


    it('button click changes props', () => {
    const { getByText } = render(<App>
                                <TestHook />
                               </App>)

    expect(getByText(/Moe/i).textContent).toBe("Moe")

    fireEvent.click(getByText("Change Name"))

    expect(getByText(/Steve/i).textContent).toBe("Steve")
    })
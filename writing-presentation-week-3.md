# Writing Rangkuman Minggu ke 3

 ## **Array dan Multidimensional Array**
- Array merupakan pengorganisasian data dan tempat penyimpanan data

- Array adalah tipe data list order yang dapat menyimpan tipe data apapun dialamnya seperti string, number, boolean dan lainnya
contoh Array

 ```javascript
    let nama = ["Anjis", 22, true ];
```

## **Memanggil Array**

  <div align="justify">
  Array pada javascript dihitung dari index data ke-0.
  Data pertama adalah index ke-0.

```javascript
  console.log(nama); //memanggil semua data
  console.log(nama[0]); //memanggil data index ke 0
  console.log(nama[1]); // memanggil data index ke 1
  console.log(nama[2]); //memanggil data index ke 2
  console.log(arr.length); //panjang data array
  ```


### **Update Array**
  <div align="justify">
  Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array

  ```javascript
  let nama = ["Anjis", 22, true ];
  nama[0] = "Anjis"
  console.log(nama)
  // output : ["Anjis", 1 , true]
  ```
- ### **Array Method**
  <div align="justify">
  Array memiliki method atau biasa disebut built-in methods, yang sama dengan function yang dapat digunakan kapan saja kita membutuhkannya.

 - **push** menambahkan array pada index terakhir
    ```javascript
    let arrHp = ["xiomy", "oppo", "samsung", "realme","iphone"]
    arrHp.push("infinix");
    
    console.log(arrHp)
    // Output : ["xiomy", "oppo", "samsung", "realme","iphone", "infinix"]
    ```
  
 - **pop** Menghapus array pada index terakhir
    ```javascript
    let arrHp = ["xiomy", "oppo", "samsung", "realme","iphone"]
    arrHp.pop();
    
    console.log(arrHp)
    // Output : ["xiomy", "oppo", "samsung", "realme"]
    ```

- **shift** Menghapus array pada index pertama

    ```javascript
    let arrHp = ["xiomy", "oppo", "samsung", "realme","iphone"]
    arrHp.shift()
    console.log(arrHp)
    // Output : ["oppo", "samsung", "realme", "iphone"]
    ```
 
 - ### **Looping pada Array**
    - Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()

        - **forEach** method untuk melakukan looping pada setiap elemen array.
            ```javascript
            let arrHp = ["xiomy", "oppo", "samsung", "realme","iphone"]
            arrHp.forEach(elemnt => {
            console.log(element); 
            })
            ```
        - **map** melakukan perulangan/looping dengan membuat array baru.

             ```javascript
             let angka = [1, 3, 4, 2]
             let double = angka.map(num =>{
                return num * 2
             })
             console.log(double)
             // Output : [2, 6, 8, 4]
             ```


## **JavaScript Object & Array of Object** <hr>
- ### **Object**
  object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)

  - **Membuat sebuah object**
    - Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel.
    - object person dengan properti

      ```javascript
      let person = {
        name : 'Anjis',
        age : 21,
        isVarified : true
      }
      ```
- ### **Mengakses Object dan Property Object**
    - **akses seluruh object**

        ```javascript
        let person = {
            name : 'Anjis',
            age : 21,
            isVarified : true
        }
        console.log(person)
       

- ### **Update Object**
  <div align="justify">
  Kita dapat melakukan update pada variabel dengan tipe data Object.

  - **Update data pada Object**
    ```javascript
    let person = {
        name : 'Anjis',
        age : 22,
        isVarified : true
    }
    person.age = 23;
    person,addres = 'Ngawi';
    console.log(person)
    /* Output :
    {
        name : 'Anjis',
        age : 23,
        isVarified : true
        addres : 'Ngawi'
    } */
    ```

    - ### **Delete Object Property**

    - Kita dapat menghapus properti dari object menggunakan delete operator.
        ```javascript
            const person = {
                name : 'Anjis',
                age : 22,
                isVarified : true
            }
            delete person.age;
            console.log(person) 
            /* Output :
            {
                name : 'Arif',
                isVarified : true
            }
        ```

- ### **Method**
    - Jika value yang kita masukkan pada property berupa function.Maka itu disebut Method.
    - Kita bisa membuat method custom untuk kita gunakan pada aplikasi kita.
    - object greeting
        ```javascript
        const greeting = {
            welcome : function () {
                return 'Hallo selamat datang';
            },
            afterTransaction : function () {
                return "terima kasih sudah membeli produk kami";
            },
        };
        console.log(greeting.welcome()); // Hallo selamat datang
        ```

- ### **Looping Object**
    - Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.
        ```javascript
        for(let key in object){
            //..
        }
        ```

## **JavaScript Rekursif** <hr>
- ### **Deskripsi Recursif**
  <div align="justify">
  Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika.<br>
  Contoh :

    ```javascript
    function reqursive(){
        // ..
        reqursive();
        // ..
    }
    ```

- ### **Ciri dari rekursif**
  - <div align="justify">Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
  - <div align="justify">Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

  ## **JavaScript Modules**<hr>
- ### **Deskripsi JS Modules**

  Js Modules adalah cara untuk memisahkan kode file yang berbeda
  - Keuntungan menggunakan modules : 
    - mudah untuk mengelola file
    - kode tidak menumpuk pada satu file
- ### **Membuat Js Modules**
    - tambahkan type= `"module"` pada script utama
        ```javascript
        <script src="indonesia.js" type="module"></script>
        ```
    - siapkan script ke-2 dan seterusnya untuk melakukan export
    - lakukan import pada file/script utama
- ### **Contoh Export Import js module**
    - script `Amerika.js`
        ```javascript
        let apple = ["iphone", "macbook", "imac"]
        export {apple}
        ```
    - script `jepang.js`
        ```javascript
        import {apple} from './amerika.js';
        console.log(apple);
        let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
        const smartPhone = ["sony", "samsung", "fujitsu", "LG"]
        let dokumenNegara = "Hello"
        export function sayHello() {
        console.log("hallooo")
        }
        let entertainment = ["anime", "manga", "wibu", "dorama"]
        // kita dapat melakukan export pada variabel, function, class
        // "export" dapat melakukan banyak export
        // "export" di tangkap (import) menggunakan kurung kurawal
        // "export default" cuma bisa 1 aja yg di export
        // "export default" ditangkap tanpa kurung kurawal
        export { motor, smartPhone as smartPhoneJepang}
        export default entertainment
        ```
    - script `indonesia.js`
        ```javascript
        // import dari file jepang dan amerika
        import Entertainment, { motor as motorJepang, smartPhoneJepang, sayHello } from "./jepang.js"
        import {apple} from './amerika.js';
        sayHello()
        console.log(Entertainment);
        console.log(smartPhoneJepang);
        console.log(motorJepang);
        motorJepang.splice(1, 1)
        console.log(motorJepang)
        console.log(apple);
        ```
        <br>

- ## **JavaScript Asynchronous**<hr>
   <div align="justify">
  Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous. Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous.


- ### **Callback**<hr>
  <div align="justify">
  Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.


- ### **Promises**<hr>
  <div align="justify"> 
  Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.<br>
  Dalam pengambilan data, promise memiliki 3 kemungkinan state.
    - Pending(sedang dalam proses)
    - Fulfilled (berhasil)
    - Rejected (gagal)

- ### **Async-Await**
  <div align="justify"> 
  Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.<br>
  
  Cara penulisan Async/await menggunakan es6 dan tidak menggunakan es6.

    ```javascript
    async function hello(){
        let result = await 'Hello'
        return result
    }
    // es 6
    const hello1 = async () => {
        let result = await 'hello'
        return result
    }
    ```
 ## **JavaScript Web Storage**<hr>

Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage.


- ### **Local Storage**

  <div align="justify">
  Dengan memanfaatkan local storage dan session storage, kita dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web.

   - Local storage memiliki karakteristik sebagai berikut:
     - Menyimpan data tanpa tanggal kadaluarsa.
     - Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
     - Dapat menyimpan data hingga 5MB.
     - Hanya dapat menyimpan data string.
     
  - **Menyimpan data pada local storage**
    <div align="justify">

    kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
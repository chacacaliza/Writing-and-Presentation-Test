# Writing and Presentation Test Week 3
## **JavaScript Intermediate**
### **Array**
- **Array** merupakan pengorganisasian data dan tempat penyimpanan data 
- Array adalah tipe data list order yang dapat menyimpan tipe data apapun dialamnya seperti string, number, boolean dan lainnya
- contoh Array 
``` 
    Let randomData = ['ini string', 20, true];
    console.log(randomData);
```
- Membuat Array : Array didefinisikan dengan square brackets []
- Mengakses Array : Array pada javascript dihitung mulai dari index ke- 0 
``` 
   Let randomData = ['ini string', 20, true];
   console.log(randomDaData[1]); //Output : 20
```
- Update Array 
```
    let arrayData =[1,2,3,4,5]

    console.log("sebelum diupdate:" arrayData[0]]);

    arrayData[0] = 15
    console.log("sesudah diupdate:" arrayData[0]]); 
```
- Const in Array
  - Apabila menggunakan let, array dapat diubah dengan nilai yang baru
  - Const tidak dapat melakukan update data. Namun dapat melakukan update konten nilai di dalam array
  - Tidak dapat mengubah array dengan array baru jika menggunakan const
 - contoh penggunaan const 
 ``` 
    const cars = ['tesla', 'honda', 'toyota'];
    cars[2] = ['nissan'];

    console.log(cars)// output : ['tesla','honda','nissan']
```
- **Array Properti**. Array memiliki 5 properti yang sering digunakan yaitu :
  - constructor
  - length
  - index 
  - input
  - prototype
- .length yaitu mengembalikan nilai dari jumlah panjang data suatu array
    ``` 
    let cars = ['tesla', 'honda', 'toyota'];
    console.log(cars.length) // output 3
    ```
- **Array Method**  atau biasa disebut dengan built in methods 
- Contoh array built in method :
    - .push adalah method untuk menambahkan item array pada urutan yang paling akhir  
    ```
     let cars = ['tesla', 'honda', 'toyota'];
     cars.push('hyundai')
     console.log(cars) // output:['tesla','honda','toyota','hyundai']
    ```
    - .pop adalah method yang menghapus item array index terakhir
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.pop()
     console.log(cars) // output: ['tesla','honda']
    ```
    - .shift adalah method untuk menghapus item array pada index pertama 
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.shift()
     console.log(cars) // output: ['honda','toyota']
    ```
    - .unshift adalah method untuk menambahkan array pada index pertama 
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.unshift('hyundai')
     console.log(cars) // output:['hyundai','tesla','honda','toyota',]
     ```
     - .sort adalah method untuk mengurutkan array secara ascending atau descending
     ``` 
     const numbers = [1,3,5,2,4];
     numbers.sort();
     console.log(numbers) // output : [1,2,3,4,5]
     ```
- **Looping pada Array**. Built in methods untuk melakukan looping pada array ada .map dan .forEach
    - .forEach adalah method untuk melakukan looping pada setiap elemen array 
    ```
    const cars = ['tesla', 'honda', 'toyota'];
    cars.forEach(element => {
    console.log(element);
    });
    ```
    - .map adalah method untuk melakukan perulangan dengan membuat array baru
    ```
    let arr = [1,2,3,4,5];
    
    let doubled = arr.map(num => {
        return num * 2;
    });
    console.log(doubled);
    ```
### **Multidimensional Array**
   > Multidimensional array bisa dianalogikan sebagai array of array
- Multidimensional array sama seperti matriks yaitu memiliki 2 dimensi (x,y)
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory);
    ```
- Mengakses multidimensional array
     ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory[1][0]);
    ```
- Penggunaan built in method pada multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.push(['Hoodie', 2]);
    console.log(inventory);
    ```
- Operation using map in multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.map(dataInventory => {
        let terjual = 100 - dataInventory[1];
        dataInventory[2] = terjual;
    });
    console.table(inventory);
    ```
   ![map array](https://user-images.githubusercontent.com/64596495/182080815-2c75210d-b973-441a-97ff-11d3ca8694c5.JPG)
- Looping pada Multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.forEach((baris) => {
        baris.forEach((column) => {
            console.table(column);
        });
    });
    ```
    ![foreach array](https://user-images.githubusercontent.com/64596495/182081356-67c6807d-1c4a-4467-885f-253039c7eb5d.JPG)


### **JavaScript Object**
- Object adalah benda mati maupun benda hidup adalah object.
Pada programming object adalah sebuah tipe data pada variabel yg menyimpan properti dan fungsi (method)
- Properti adalah data lengkap dari sebuah object
- Method adalah action dari sebuah object. 
- Contoh object 
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    ```
- Cara mengakses object  
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    console.log(person);
    ```
- Cara mengakses properti pada object
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    console.log(person.name)
    ```
- Saat pemanggilan properti object dapat menggunakan bracket notation
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        'current address': 'Malang','JawaTimur'
    }
    console.log(person['name'])
    ```
- Update object 
  - Object dapat mengupdate value dari key yang sudah tersedia
  - Object dapat menambah key dan value baru
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    person.age = 23;
    console.log(person);
    ```
- Delete object properti
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    delete person.age;

    console.log(person);
    ```
- Method : jika value yang dimasukkan pada properti berupa function 
- console adalah global javascript object dan log adalah properti yang berupa function dari object console
- Nested Object
- Pass by reference : mengubah data pada object melalui function dan memasukkan object sebagai parameter function
- Looping pada object
- Array of object

### **Git dan Github** 
- GIT log : untuk melihat history perubahan yang telah dilakukan pada suatu project
- GIT checkout : untuk berpindah branch atau membuat branch baru
- GIT reset    : untuk merubah ke commit sebelumnya
- GIT Revert : untuk membatalkan perubahan yang terjadi di git tanpa menghapus git commit sebelumnya
- Clone yaitu menggandakan atau mengcopy sebuah project
- Fork yaitu sama halnya dengan clone namun langsung mengambil file dari repository

### **JavaScript Recursive**
- Recursive adalah fungsi yang memanggil dirinya sendiri sampai suatu kondisi tertentu terpenuhi
- A new paradigm :
  - Procedural
  - Conditional
  - Looping
  - Modular (function)
  - Recursive
- Ciri dari recursive:
  - Fungsi recursive memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. 
  - fungsi recursive selalu memaanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.
- Contoh mencari nilai pangkat 
    ```
    function pow(x,n) {
        if (n=1){
            return x;
        } else {
            return x * pow(x, n-1);
        }
    }
    console.log(pow(2,3)) // 8
    ```

### **JavaScript REGEX**
- **Regex** adalah susunan karakter/karakter spesial yang menggambarkan pattern/pola untuk pencarian text pada sebuah string atau document
   > REGEX = Text Matching
- Contoh penggunaan Regex :
  - Validasi input dari sebuah form
  - Mencari keyword tertentu pada email atau halaman web
  - Mencari IP adress dalam kisaran tertentu
- Membuat Pola Regex
  - Literals adalah konsep regex adalah konsep yang paling sederhana yaitu dengan membuat regex sesuai dengan text yang ingin dicari
- Built in Method Regex
  - test() yaitu built in method untuk regex yang mengembalikan nilai Boolean untuk kecocokan sebuah nilai yang dicari
    ``` 
    let regex1 = new RegExp('Cat');
    console.log(regex1.test('Cat'))// true
    ```
  - Karakter Set digunakan untuk mencari minimal 1 karakter yabg sesuai. Karakter set menggunakan bracket square []
    ``` 
    let regex1 = new RegExp('[a-z]');
    console.log(regex1.test('abc'))// true
     ```
  - match() yaitu method yang mengembalikan nilai array dari karakter yang match
    ``` 
    let myRegex = /c/;
    let myName = 'Chaca';
    console.log(myName.match(myRegex)); // output : [ 'c', index: 3, input: 'Chaca', groups: undefined ]
    ```
   - Flags pada javascript :
     - i : untuk menghandle case-sensitive. Tidak mempermasalhkan besar kecilnya karakter
     - g : untuk mencari kedalam seluruh string yang ingin dicari. Jika tidak menggunakan flags g maka sistem akan mengembalikan nilai array pertama yang ditemukan tanpa melanjutkan pencarian
      ```
      let myRegex = /c/ig;
      let myName = 'Chaca';
      console.log(myName.match(myRegex)); 
      // output : [ 'c', index: 3, input: 'Chaca', groups: undefined ] // output: [ 'C', 'c' ]
      ```
- Karakter Set Short Syntax  
  - \d : seluruh number/digit character
  - \w : alphanumeric character
  - \s : whitespace character (space,tab,newline)
    ``` 
    let myRegex = /\d\s\w\w\w\w\w\w\w/;
    let myName = '3 Kelinci';
    console.log(myRegex.test(myName));// true
    ```
  - Negasi dari set short syntax yaitu menggunakan tanda ^
    ``` 
    let notBinary = /[^01]/
    console.log(notBinary.test['1012']) // true
    ```
  - Quantifiers berfungsi untuk membuat format regex menjadi lebih rapi. 
  - Quantifiers ditandai dengan format {} 
  contoh saat mencari roa{3}r maka akan match dengan string 'roaaar'
  - Quantifiers besifat greedy akan mengambil nilai yang paling besar atau maksimal
  contoh saat mencari roa{3,5}r maka akan match dengan 'roaaar' dan 'roaaaaar' maka yang akan didapatkan adalah yang 'roaaaaar'
  - Anchor yaitu digunakan jika ingin mencari karakter yang sama persis. 
  - Anchor diawali dengan ^ dan diakhiri dengan $
  - Alternation yaitu digunakan untuk mencari karakter yang sama persis dengan lebih dari 1 kalimat
  - Alternation ditandai dengan format (|)
    ``` 
    let search = /^Belajar javascript san react js$ |^ React JS$/
    console.log(search.test{'React JS'}); output : true
    ```

### **JavaScript OOP**
- **OOP** atau Object Oriented Programming adalah suatu paradigma dalam pemrograman 
- 4 Pilar dalam OOP :
  - Encapsulation adalah cara untuk membatasi akses langsung ke properti atau method dari sebuah objek
    ```
        function Gojek(jarak) {
        const pricePerKm = 4000;
        this.jarak = jarak;

        this.price = function () {
        return pricePerKm * this.jarak;
        };
        }

        let gojek1 = new Gojek(10);
        gojek1.pricePerKm = 10000;

        console.log(gojek1.price());
     ```
  - Inheritance adalah sebuah proses dimana sebuah kelas mewariskan properti dan method ke kelas lain atau childnya
     ```
        class Person {
        constructor(name, age) {
          this.name = name;
          this.age = age;
        }
        greeting() {
        return `Hello ${this.name} umur ${this.age}`;
        }
        }
        class PNS extends Person {
        constructor(name, age, nik, lokasiPenempatan) {super(name, age);
        this.nik = nik;
        this.lokasiPenempatan = lokasiPenempatan;
        }
        detail() {
        return `Hello ${this.name} umur ${this.age} dengan nik ${this.nik} penempatan ${this.lokasiPenempatan}`;
        }
        }
        let pns1 = new PNS("Chaca Caliza", 22, 081119999, "Surabaya");

        console.log(pns1.detail());
     ``` 
  - Polymorpishm adalah kemampuan dari suatu objek untuk memiliki banyak bentuk
     ```
        class Animal {
        sound() {
        console.log("Animal Make sound");
        }
       }

        class Cat extends Animal {
        sound() {
        console.log("Miaw");
        }
       }
       
       class Cow extends Animal {
        sound() {
         console.log("Mooo");
        }
        }
        let anggoraCat = new Cat();
        let sayCow = new Cow();

        angoraCat.sound();
        sayCow.sound();
     ```
  - Abstraction adalah teknik untuk menyembunyikan detail tertentu dari sebuah object atau method dan hanya menampilkan fitur penting dari objek tersebut

### **JavaScript Modules**
- Modules memungkinkan untuk memecah kode menjadi file terpisah sehingga mempermudah untuk maintain code
- JavaScript Module bergantung pada pernyataan impor dan ekspor

### **WEB STORAGE**
- Web Storage adalah wadah untuk sebuah data yang digunakan untuk penyimpanan data yang terikat di browsernya
- Jenis Web Storage yang umum digunakan yaitu :
  - Local Storage
  - Session storage
  - IndexDB
  - Cookies
- Cara menyimpan data pada local storage 
    ```
        let token = "asdfghjkl" //key
        localStorage.setItem("token", token);
    ```
- Cara mengambil token
    ```
        localstorage.getItem("token", token);
        console.log(localStorage.getItem('token");
    ```
- Cara menghapus data 
    ```
        localStorage.removeItem("token")
    ```
### **Asynchronous**
- Asynchronous sebuah teknik yang menyelesaikan fungsi secara paralel
- Penggunaan asynchronous dapat dilakukan jika kita ingin mengambil data dari database
- Mengapa perlu menggunakan asynchronous? Asynchronous dibutuhkan ketika ada proses yangg membutuhkan waktu lama. Jadi kita bisa mengerjakan proses yg lain secara paralel.
- Callbacks adalah suatu function namun cara pengeksekusiannya yang berbeda yaitu hanya mengeksekusi pada point tertentu.
- Salah satu function yang digunakan untuk mengatur penjadwalan asynchronous adalah **setTimeout** function
- contoh penggunaan asynchronous
  ```
    function p1() {
    console.log('p1 done')
  }
    function p2() {
    setTimeout(
      function() {
        console.log('p2 done')
      },2000
    )
  }
  function p3() {
  console.log('p3 done')
  }
  p1()
  p2()
  p3()
  ```
- Contoh Penggunaan Callback pada Asynchronous
  ```
    function p1() {
    console.log('p1 done')
  }

    function p2(callback) {
    setTimeout(
    function() {
    console.log('p2 done')
      callback()
    },100
    )
  }

  function p3() {
  console.log('p3 done')
  }
  p1()
  p2(p3)
  ```
- **Asynchronous - Promise** merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason)
  ```
    function GetUser(id) {
    return new Promise((resolve, reject) => {
    if (id !== "" && id !== undefined) {
      reesolve (id);
    } else {
      reject ("ID Harus di Isi");
        }
    });
    }
    
    GetUser( ) 
    .then((response) => {
    console.log(response);
     })
     .catch((error) => {
    console.log(error);
    });
  ```
- **Asynchronous - Async-Await** merupakan fitur yang hadir sejak ES2017 bekerja dengan cara menunda eksekusi hingga proses asynchronous selesai
- **Asynchronous - Fetch** merupakan cara baru dalam melakukan network request yang memanfaatkan sebuah Promise dalam penggunaanya. Karen Fetch mengembalikan sebuah Promise maka respon handling yang digunakan adalah **then** jika promise mengembalikan resolve dan **catch** jika promise mengembalikan nilai reject
  ```
    fetch("https://pokeapi.co/api/v2/pokemon/pikachu/", {
    method: "GET"
    })
     .then((response) => {
      return response.json();
    })
    .then((data) => {
     console.log(data);
     })
    .catch((error) => {
    console.log(error);
    });
  ```
- **API dan HTTP Request**
   > API : Application programming interface
 - API sebagai alat untuk berbicra antar perangkat lunak 
 - API dapat digunakan untuk sistem berbasis web,sistem operasi, sistem basis data dan perangkat lunak
    > HTTP : Hypertext transfer protocol
 - HTTP di desain untuk memungkinkan komunikasi antar klien dan server. 
 - HTTP berfungsi sebagai protokol Request-Response antara klien dan server. 
 - HTTP Request yaitu Keadaan dimana server membaca apa yang dikirimkan oleh client melalui aplikasi web server
 - HTTP Method :
   - GET digunakan untuk meminta data dari sumber tertentu
   - POST digunakan untuk mengirim data ke server untuk membuat/memperbarui resource
   - PUT digunakan untuk mengirim data ke server untuk membuat/memperbarui resource.
   - DELETE untuk menghapus spesifiksi resource


    


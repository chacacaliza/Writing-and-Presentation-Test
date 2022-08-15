# Writing and Presentation Test Week 4
### **Asycnhronous**
- Promise 
  ```
     function GetUser(id) {
       return new Promise((resolve, reject) => {
      if (id !== "" && id !== undefined) {
       resolve (id);
      } else {
      reject ("ID Harus di Isi");
       }
     });
    }
    
    GetUser( ) // memanggil fungsinya GetUser
    .then((response) => {
     console.log(response);
     })
    .catch((error) => {
    console.log(error);
    });
   ```
- Fetch
  ```
    fetch("https://pokeapi.co/api/v2/pokemon/pikachu/", {
    method: "GET"
    })
     .then(async (response) => {
    let convertData = await response.json();
    console.log(convertData);
    })
    .catch((error) => {
    console.log(error);
    });
  ```
- HTTP Request yaitu berfungsi sebagai alat komunikasi froentend dengan backend
- HTTP Request Method
   - GET untuk mengambil data 
   - POST untuk mengirimkan data
   - PUT untuk mengirimkan atau memperbaharui data
   - DELETE untuk menghapus data
 
 ### **Responsive Web Design**
- **Responsive Web Desin** yaitu suatu tampilan website yang dapat menyesuikan dengan perangkat yang digunakan
- Chrome Dev Tools merupakan tools pada google chrome yang digunakan sebagai tools Responsive Web Design
- Untuk mengakses Chrome Dev Tools yaitu 
  > ctrl + shift + j
  > ctrl + shift + m digunakan untuk melihat toggle bar 
- Dalam menggunakan Responsive Web Design pada bagian HTML perlu ditambahkan **viewport** pada bagian head agar tampilan website dapat menyesuaikan dengan berbagai device
- Untuk membuat suatu gambar pada halaman website agar menjadi responsive dapat dilakukan dengan menambahkan atribut Max - width = 100% pada bagian gambar
- **Media Query** salah satu cara untuk mengatur suatu website agar bisa terdiri dari beberapa jenis 
- Penggunaan media query yang umum digunakan adalah min-width dan max-width
- Contoh penerapan media query 
  `` @media screen and (max-width: 500px)``
- Cara mengkondisikan Media Query ada 2 cara yaitu:
  - Memisahkan beberapa file css sesuai dengan tampilan device yang ingin dibuat 
  - Menggabungkan semua styling css device menjadi 1 
- Breakpoint yaitu istilah saat terjadi perubahan ukuran pada suatu website ketika berganti device
- Terdapat 3 jenis breakpoint yaitu desktop, tablet, dan mobile phone
- Penggunaan breakpoint pada media query dapat dilakukan dengan membuat range ukuran sesuai dengan tampilan device yang ingin dibuat
- Contoh breakpoint dapat ditulis seperti ini
  ```
  @media screen and (min-width: 500px) and (max-width: 700px) {
  body {
    background-color: grey 
    }
   }
  ```
### **Bootstrap**
- Bootstrap adalah salah satu framework opensource yang berfungsi membuat suatu responsive website
- Komponen utama bootstrap :
  - bootstrap.css
  - bootstrap.js
- Cara konfigurasi bootstrap :
  - Membuat tag boostrap di head. Cara memanggil css bootstrap dengan menggunakan href lalu mengganti link href css lokal dengan link boostrap online.
- Kapan kita menggunakan bootstrap?
  - Boostrap digunakan ketika membuat website sederhana dan tidak memerlukan load lama
- Layout pada boostrap :
  - Breakpoints merupakan suatu cara yang dilakukan untuk membuat desain responsif dengan mengontrol kapan tata letak yang disesuaikan dengan ukuran perangkat
    tertentu.
  - Breakpoints pada bootstrap ada 5 yaitu sm, md, lg, xl dan xxl.
  - Setiap breakpoint dipilih untuk menampung container yang lebarnya 12 dengan sehingga tersusun rapi. Breakpoint juga mewakili subset ukuran perangkat umum dan
    dimensi area pandang.
  - Container adalah blok dasar atau pembungkus boostrap yang terdiri dari contain, pad dan align  yang menyelaraskan konten website dalam perangkat atau area      
    pandang tertentu.
  - Terdapat 3 container pada boostrap yaitu :
    - .container, yang menerapkan lebar maksimum pada setiap breakpoint responsif
    - .container-{breakpoint}, menerapkan lebar 100% sampai dengan breakpoint yang ditentukan.
    - .container-fluid, menerapkan 100% ukurannya dari breakpoints
  - Grid System pada bootstrap yang terdiri dari 12 kolom default.
  - Grid system pada bootstrap menggunakan container,baris dan kolom untuk menata dan menyelaraskan konten,yang dibangun menggunakan flexbox dan itu sudah responsive.
  - 

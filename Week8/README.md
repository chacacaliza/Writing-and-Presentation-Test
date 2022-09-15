# Writing and Presentation Test Week 8
## **State Management Redux**
- Redux digunakan untuk mengolah state management
- State management pada dasarnya adalah cara untuk memfasilitasi komunikasi dan berbagi data di seluruh komponen.
- Redux Memudahkan User dalam :
  - menyimpan status aplikasi Anda. 
  - mengelola status aplikasi Anda. 
  - memberi tahu pihak yang berkepentingan ketika status aplikasi berubah.
- Redux memungkinkan untuk mengelola status aplikasi Anda di satu tempat dan membuat perubahan di aplikasi mudah untuk diprediksi dan dilacak
- Redux thunk adalah middleware yang memungkinkan untuk memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. 
- Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
- Untuk penggunaan redux thunk dengan `` npm install redux-thunk@2.3.0 ``
## **React Context**
- React Context dirancang untuk berbagi data yang dapat dianggap "global" untuk pohon komponen React, seperti pengguna yang diautentikasi saat ini, tema, atau bahasa pilihan
- Penggunaan React Context 
  - Untuk membuat new context, gunakan fungsi createContext baru React: `` export const LocaleContext = React.createContext('en'); ``
  - Fungsi createContext mengembalikan a Provider dan a Consumer component..

## **React Testing**
- Testing berarti memeriksa bahwa kode kami memenuhi beberapa harapan
- Testing dibagi menjadi 2 main kategori yaitu :
  - Unit Testing
  - integration testing
  - UI texting
- **Unit Texting** menggunakan Jest adalah a JavaScript test runner, yaitu library JavaScript untuk membuat, menjalankan, dan menyusun pengujian.
- Unit texting ini, unit individu atau komponen perangkat lunak diuji. Sebuah unit dapat berupa fungsi individu, metode, prosedur, modul, atau objek. Tes unit mengisolasi bagian kode dan memverifikasi kebenarannya, untuk memvalidasi bahwa setiap unit kode perangkat lunak berfungsi seperti yang diharapkan.
- Terdapat 2 scenario yang dilakukan dalam melakukan unit testing yaitu:
  - mewarisi kode warisan yang datang tanpa tes
  - menerapkan fungsi baru secara tiba-tiba
- Alur testing:
  - impor fungsi untuk menguji 
  - Memberikan masukan ke fungsi 
  - Menentukan apa yang diharapkan sebagai output 
  - Memeriksa apakah fungsi menghasilkan output yang diharapkan
- Mengapa perlu dilakukan testing:
  - Tujuan pertama dari testing adalah untuk mencegah regresi. Regresi adalah kemunculan kembali bug yang sebelumnya telah diperbaiki. Itu membuat fitur berhenti berfungsi sebagaimana dimaksud setelah peristiwa tertentu terjadi
  - Testing digunakan memastikan fungsionalitas komponen kompleks dan aplikasi modular.
  - Testing diperlukan untuk kinerja yang efektif dari aplikasi perangkat lunak atau produk.
- React Testing Library dibangun di atas DOM Testing Library dengan menambahkan API untuk bekerja dengan komponen React.
- Menginstall library testing ``npm install --save-dev @testing-library/react``
- 

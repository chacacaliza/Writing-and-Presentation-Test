# Writing and Presentation Test Week 7
## **React JS Lanjutan**
### **Hooks**
- Hooks merupakan fitur terbaru pada React yang berguna untuk melakukan state management dan side effects di dalam function component.
- Kelebihan menggunakan hooks adalah code yang digunakan akan lebih pendek, clean dan mudah dimengerti.
- Jenis Hooks yang sering digunakan yaitu useState dan useEffect.
- **Use State**
- pada hooks digunakan untuk membuat dan mengupdate state.
- Contoh code 
  ``` 
  import React, { useState } from 'react';
  export default function App() {
  const [state, setState] = useState('Chaca');
  const handleChange = () => {
    setState('Caliza');
  };
  return (
    <div>
      <h1>Hello Devsaurus</h1>
      <p>My Name is {state}</p>
      <button onClick={handleChange}>Change Name</button>
    </div>
      );
    }
  ```
- Penggunaan useState pada hooks biasanya digunakan untuk penyimpanan data pada form yang selanjutnya data tersebut akan di post ke api lalu dproses.
- **Use Effect**
- Hooks yang digunakan untuk menggunakan lifecycle pada functional component dengan mudah.
- Lifecycle pada hooks hanya menggunakan useEffect yang menyatukan component DidMount, ComponentDidUpdate dan componenetWillUnmount.
- side effect pada react adalah function yang dieksekusi setelah render yang biasanya ditempatkan dibawah state
- Contoh code 
  ```
   import React, { useState, useEffect } from 'react';

   function Example() {
   const [count, setCount] = useState(0);

   // Mirip dengan componentDidMount dan componentDidUpdate:
   useEffect(() => {
    // Memperbarui judul dokumen menggunakan API browser
    document.title = `You clicked ${count} times`;
    });

    return (
    <div>
     <p>You clicked {count} times</p>
     <button onClick={() => setCount(count + 1)}>
        Click me
     </button>
     </div>
    );
  }
  ```
- **Prop Types**
- PropTypes merupakan sebuah library yang dapat membantu dalam memeriksa tipe data props yang apabila tidak sesuai maka akan memunculkan pesan error
- Contoh code 
  ```
  import React from 'react';
  import PropTypes from 'prop-types';
  const User = (props) => {
  const { name } = props;
  return (
    <>
      <h1>My Name is {name}</h1>
    </>
  );
  };
  export default function App() {
  return (
    <div>
      <h1>Hello Devsaurus</h1>
      <User name="brachio" />
    </div>
    );
  }
  User.propType = {
  name: PropTypes.string
  };
  ```
- ###**Router**
- React Router merupakan standar library untuk routing pada React.
- standar routing berfungsi untuk membuat suatu website menjadi dynamic.
- Pada React, Router membantu untuk mengarahka page satu ke page yg lainnya berdasarkan path url yg ditentukan.
- Cara menginstall/menggunakan React Router : 
  - npm install react-router-dom@6
  - Menambahkan import { BrowserRouter } from "react-router-dom"; pada bagian index.js
  - Menambahkan code :
  ```
   <BrowserRouter>
      <App />
    </BrowserRouter>
  ```
- Browser Router merupakan interface pada umumnya yg digunakan  untuk menjalankan react di browser atau untuk membuat router-router sederhana.
- HashRouter penulisannya menggunakan #, yg digunakan pada sebuah website yang menggunakan satu page saja.
- Code pada Bagian App.js
  ```
  import React from 'react'
  import { BrowserRouter, Route, Switch } from 'react-router-dom'

  import Notfound from './pages/NotFound'
  import Home from './pages/Home'
  import Profil from './pages/Profil'
  import ProfilDetail from './pages/ProfilDetail'

  function App() {
    return (
      <BrowserRouter>
        <Switch>
          <Route path="/" exact component={Home} />
          <Route path="/profil" exact component={Profil} />
          <Route path="/profil/:name" exact component={ProfilDetail} />
          <Route component={Notfound} />
        </Switch>
      </BrowserRouter>
    )
  }

  export default App
  ```
- Code pada Bagian Page Home
  ``` 
  import React from 'react'
  import { Link } from 'react-router-dom'

  function Home(props) {
    return (
      <>
        <h2>
          Home page
        </h2>

        <Link to="/profil">Menuju profil</Link>
      </>
    )
  }
  ```
- 3 cara penggunaan router :
  - Routing Dasar
  - Dynamic Route
  - Nested Route
  
-###**React Redux**
- Redux digunakan untuk mengolah state management
- Yaitu dengan menyimpan state di satu tempat, sehingga lebih mudah untuk di manage.
- cara kerja Redux :
  - Action : Adalah sebuah function yang mereturn sebuah objek.
  - Reducer : sebuah fungsi yang tugasnya untuk mengolah state yang ada di store.
  - Store : tempat untuk menampung state
   

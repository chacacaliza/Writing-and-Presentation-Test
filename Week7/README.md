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
### **Router**
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
  
- Contoh Penulisan Code Dynamic Router
  ```
    import {Link,Route, Routes} from 'react-router-dom';
    import Artist from './Artist';
    import './App.css';
    
    function App() {
    return (
    <>
    <ul>
    <li><Link to="/artist/Ariana">Ariana</Link></li>
    <li><Link to="/artist/Taylor">Taylor</Link></li>
    <ul>
    
    <Routes>
    <Route path="/artist/:name" element={<Artist />}/>
    </Routes>
    </>
     );
    }
  ```
- Contoh Penulisan Code Nested Route
  ```
    import User from './user/User';
    import Setting from './user/setting/Setting';
    import Profile from './user/profile/Profile';
    import Favorite from './favorite/Favorite';

    function App() {
      return (
        <>
      <ul className='user'>

      <li><Link to="/">Home</Link></li>
      <li><Link to="/user">User</Link></li>
      <li><Link to="/favorite">FavoriteKu</Link></li>
      <li> <Link to="/galeri">Galeri</Link></li>
      </ul>

      <Routes>
            <Route path='/' element={<Home/>}/>
            <Route path='/User' element={<User/>}/>
            <Route path='/Gallery' element={<Gallery/>}/>
            <Route path='/Favorite' element={<Favorite/>}/>

            {/* Nested router */}
            <Route path='/Favorite/Music' element={<Music/>}/>
            <Route path='/User/Profile' element={<Profile/>}/>
            <Route path='/User/Settings' element={<Settings/>}/>
      </Routes>
       </>
      );
    }

   ```
### **React Redux**
- Redux digunakan untuk mengolah state management
- Yaitu dengan menyimpan state di satu tempat, sehingga lebih mudah untuk di manage.
- cara kerja Redux :
  - Action : Adalah sebuah function yang mereturn sebuah objek.
  - Reducer : sebuah fungsi yang tugasnya untuk mengolah state yang ada di store.
  - Store : tempat untuk menampung state
- Contoh React Redux
  - Setup Store di App.js
 ```
  import { createStore } from "redux";
  import { composeWithDevTools } from "redux-devtools-extension";
  import rootReducer from "./reducers"; 
  const store = createStore(
  rootReducer,
  composeWithDevTools()
  )
  export default store;
 ```
  - Membuat reducer pada untuk todolist di src/store/reducers/todoReducer.js.
 ```
    const initialState = {
    todos: [
      {
        id: 1,
        title: "title one",
        completed: false
      },
      {
        id: 1,
        title: "title one",
        completed: false
      }
    ]
  }
  const todoReducer = (state = initialState, action) => {
    const { type, payload} = action;
    switch(type){
      default:
        return {
          ...state
        }
    }
  }
  export default todoReducer;
```
 - Menggabungkan reducer-reducer didalam file src/store/reducers/index.js
```
  import { combineReducers} from "redux";
  import todoReducer from "./todoReducer";
  export default combineReducers({
  todoReducer
  })
```
 - Menghubungkan redux dan app reeact di file app.js
```
  import React from "react";
  import { Provider} from "react-redux";
  import store from "./store"
  const App= () => {
    return(
      <Provider store={store}>
        <div>
          <TodoApp/>
        </div>
      </Provider>
    )
  }
  export default App;
```
 - Menggambil data dari store
```
  import React from "react";
  import { connect } from "react-redux";
  const TodoApp= ({ todos }) => {
    return(
      <div>
        <h1>todo app</h1>
        {todos.map(todo =>
          <div key={todo.id}>
            <p>{todo.title}</p>
          </div>
        )}
      </div>
    )
  }
  const mapStateToProps = state => ({
    todos: state.todoReducer.todos
  })
  export default connect(mapStateToProps)(TodoApp);
```

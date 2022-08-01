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
 

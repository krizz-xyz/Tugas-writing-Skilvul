# <center style="background-color:tomato;">**Writing & Presentation Week 3**

### **JS ARRAY and JS ARRAY Multidimensi**
1. Array merupakan sebuah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya yang berupa String, Number, Boolean, dan lainnya.
2. Contoh Struktur array :
    ```javascript
        let nama = ["Rohmad Krisna", 21, true ];
    ```

    Varible yang mempunyai beberapa index yang dimulai dari index ke-0 dihitung dari kiri. Dan cara mengakses atau memanggil array sebagai berikut :
    ```javascript
        console.log(nama);
        console.log(nama[0]);
        console.log(nama[1]);
        console.log(nama[2]);
    ```

3. Array Multidimensi adalah array didalam array atau bisa dianalogikan dengan array of array.

4.  contoh struktur dalam array multidimensi adalah 
    ```javascript
        let nama =[
                ["krizz", 21, true ],
                ["putra", 10, false ],
                ["tri", 20, false ],
        ];
    ```

5. Cara mengakses array multidimensi adalah :
    ```javascript
        console.log(nama[0][2]);
        console.log(nama[1][1])
        console.log(nama[2][0])
    ```

6. Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype. Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.


7. Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.

 
## JS Intermeidiate-Object
1. Object adalah dalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Object kita dapat menyimpan properti dengan tipe data apapun.


2. contoh struktur object 
    ```javascript
        let hewan = {
            nama = `ikan`,
            jenis = `cupang`,
            jumlah = 4,
        };
    ```
3. Cara memanggil object dan mengaksesnya 
    ```javascript
        console.log(hewan);
        console.log(hewan.nama);
        console.log(hewan.jenis);
        console.log(hewan.jumlah);
    ```
4. Kita bisa mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function. Pada real application nanti kalian pasti menemukan data object yang kompleks. Object yang berasal dari turunan object lainnya. Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping. Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.



## JS Intermeiadte-Recursive
1. Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Yang kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.

2. Struktur rekursiv
    ```javascript
        function rekursiv(){
            if(){
            
            } else {
                rekursiv();
            }
            }
      ```

3. Ciri - ciri rekursif sebagai berikut : <br>
    * Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
    * Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

4. Contoh penerapan rekursiv
    ```javascript
        function deretAngka(n){
          if (n == 1) {
            console.log(n)
          } else {
            deretAngka(n-1)
            console.log(n);
          }
        }
        
        console.log(5)    
    ```

5. Rekursif ini bisa dilakukan dengan looping atau if statement.


## JS Intermeiadte-Asynchronous-Introduction and Promise

1. Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung. Yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa. Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous.

2. Membuat asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara: <br>
    * Callback
    * Promises
    * Async/Await

3. Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya. 
    ```javascript
        setTimeout(() => {
            console.log("B")
            }, 1000)

            console.log("C")
    ```
4. Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API. 
    ```javascript
        let nontonPromise = new Promise((resolve, reject) => {
        if (true) {
            resolve("nonton terpenuhi") // berhasil
          } 
        reject("gagal"); // gagal
        });
    ```
     

1. Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
    ```javascript
        async function asyncNonton() {
        try {
            let result = await nonton("jalan")
            console.log(result);
              } catch (error) {
                    console.log(error)
              }
            }
            asyncNonton()
    ```
    
6. Fetch adalah native web API untuk melakukan HTTP calls dari external network.
    ```javascript
        fetch("https://digimon-api.vercel.app/api/digimon")
        .then(result => result.json())
        .then(result => {
          console.log(result)
        })
    ```
    fetch() memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body. Tergantung keinginan kita.

    cotoh penerapan nya :<br>
    ```javascript
        let asyncApi = async() => {
        let api = ("url");
        let option = {
            method: "GET"
        }
        let response = await fetch(api, option)
        response = await response.json()
        console.log(response);
        }
        asyncApi();
    ```

## JS Intermediate Web Storage
1. Web Storage adalah menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.


2. Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah.

3. Local storage memiliki karakteristik sebagai berikut: <br>
    * Menyimpan data tanpa tanggal kadaluarsa.
    * Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
    * Dapat menyimpan data hingga 5MB.
    * Hanya dapat menyimpan data string.

4. Struktur dasar local storage 
    ```javascript
        if (localStorage.getItem("theme") === "dark") { 
    document.body.classList.add("dark");
    } else {
      document.body.classList.remove("dark");
    }

    document.getElementById("toggle").onclick = () => {
      if (localStorage.getItem("theme")) {
        localStorage.removeItem("theme");
        document.body.classList.remove("dark");
        } else {
        localStorage.setItem("theme", "dark");
        document.body.classList.add("dark");
        }
        };
    ```
 
#
# Laporan Praktikum week 1
Nama : Jein Ananda

Nim : 10221031


## Soal
1. Tuliskan pengalaman belajar mulai dari awal praktikum hingga praktikum selesai. Bisa menyertakanan screenshot, atau potongan kode selama praktikum.
2. Berikan kelebihan dan kekurangan menggunakan browser dan Node.js.
3. Jalankan program berikut melalui Node.js
```js
let randomQuote;
const quotes = [
  "The best way to predict the future is to create it.",
  "Be the change you wish to see in the world.",
  "Innovation distinguishes between a leader and a follower.",
  "Believe you can and you're halfway there.",
  "Your time is limited, don't waste it living someone else's life."];

randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
console.log(randomQuote);
```
Selanjutnya apakah yang terjadi jika secara terus menerus hanya menjalankan dua baris terakhir?

### Jawaban
1. Pengalaman yang saya dapatkan adalah dapat mempelajari dasar dasar awal bahasa pemrograman javascript yang mana itu cukup asing bagi saya , karena selama libur semester saya justru belajar c++ karena mendapatkan kabar bahwa semester 2 menggunakan c++ namun ternyata justru menggunakan javascript , dan ternyata javascript tidak sesulit yang saya kira dan saya cukup enjoy melakukan coding menggunakan javascript. adapun percobaan percobaan yang saya lakukan setelah praktikum berdasarkan yang telah kak Feriyanto ajarkan seperti

    1. Melakukan syntax console.log untuk menampilkan teks ke console , berikut code nya 
    ```js
    console.log("Made by Jein")
    ```
    2. Membuat button onclick beserta fungsi nya dimana untuk fungsi nya saya lakukan di JS dengan mengambil referensi soal ke 3 
    ```js
    <html>
    <head>
        <title>Testing zone</title>
    </head>
    <body>
        <h1>Quotes Generator by Jein</h1>
        <div id="quoteDisplay"></div>
        <button onclick="newquote()">New Quotes</button>
        <script src="test.js"></script>
    </body>
</html>
code di atas untuk html , dan untuk JS nya ada di bawah

```js
var quotes = [
    "Believe you can and youre halfway there",
    "The best way to predict the future is to invent it",
    "Happiness is not something ready made It comes from your own actions",
    "I have not failed Ive just found 10,000 ways that wont work",
]

function newquote(){
    var random = Math.floor(Math.random() * (quotes.length));
    document.getElementById('quoteDisplay').innerHTML = quotes[random];
}
```
dimana untuk penjelasan nya saya membuat variables quotes yang berisikan 4 quotes yang lalu saya membuat fungsi newquote untuk mengenerate random quote berdasarkan variable quotes yang sudah saya buat, untuk hasil screenshot nya ada di bawah ini

ini adalah ss sebelum mengclick button New Quotes
<img src="Screenshot (1004).png" alt="" width="900">

dan ini adalah ss setelah mengclick button New Quotes
<img src="Screenshot (1005).png" alt="" width="900">



2. Browser dan Node.js adalah dua platform perangkat lunak yang berbeda dengan tujuan dan fungsionalitas yang berbeda. Berikut adalah kelebihan dan kekurangan dari masing-masing platform


- **Kelebihan Browser :**

 *Mudah diakses Browser seperti Chrome, Firefox, Safari, dan lainnya sudah tersedia dan mudah diakses di banyak perangkat.*

 *User Interface Browser menyediakan antarmuka yang mudah digunakan untuk interaksi pengguna dengan situs web dan aplikasi web.*

 *Kompatibilitas Browser diinstal pada berbagai sistem operasi dan menawarkan kompatibilitas yang baik dengan banyak teknologi web seperti HTML, CSS, dan JavaScript.*

- **Kekurangan Browser :**
 *Keterbatasan Lingkungan - Browser hanya dapat menjalankan aplikasi web dalam lingkungan yang terisolasi dari sistem operasi.*

 *Keterbatasan akses ke Sumber Daya Sistem - Browser memiliki keterbatasan dalam hal akses ke sumber daya sistem seperti file sistem, database, dan perangkat keras.*

 *Keterbatasan Kinerja - Karena browser harus berjalan di atas sistem operasi, mereka tidak dapat memanfaatkan sumber daya sistem secara langsung dan seringkali memiliki keterbatasan kinerja yang lebih rendah dibandingkan dengan aplikasi desktop yang sama.*

- **Kelebihan Node.js :**

 *Scalability - Node.js dapat menangani permintaan yang lebih banyak dengan efisien karena kemampuan asinkronous I/O yang baik.*

 *Cross-platform - Node.js berjalan di berbagai sistem operasi, sehingga aplikasi dapat dikembangkan dan dideploy pada berbagai platform.*

 *Pustaka Modul - Node.js menawarkan ribuan modul pustaka open-source yang memudahkan pengembangan dan mempercepat waktu pengembangan.*

- **Kekurangan Node.js :**

 *Sulit untuk aplikasi yang membutuhkan akses ke sumber daya sistem - Node.js memiliki keterbatasan dalam mengakses sumber daya sistem seperti file sistem, database, dan perangkat keras.*

 *Masalah skala vertikal - Node.js memiliki batasan dalam skala vertikal, yang dapat membuat pengembangan aplikasi yang sangat besar menjadi sulit.*

 *Single Threaded - Node.js berjalan pada thread tunggal, yang berarti bahwa pengguna harus hati-hati dalam menangani tugas-tugas yang berat dan jangan membuat kesalahan dalam memprogram.*
 
 
 
3. Jika hanya menjalankan dua baris terakhir secara terus menerus, maka setiap kali program dijalankan, ia akan menampilkan kutipan acak dari larik kutipan yang didefinisikan di atas menggunakan fungsi Math.random() untuk memilih sebuah kutipan secara acak. Setiap pengulangan akan menghasilkan kutipan yang berbeda karena kutipan dipilih secara acak. Tidak akan ada perubahan atau pengaruh pada array kutipan karena array hanya didefinisikan satu kali pada awal program dan tidak dimodifikasi lagi.*
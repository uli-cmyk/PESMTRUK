# Laporan Praktikum week 3
Nama : Jein Ananda

Nim : 10221031

## Soal 

1. Carilah satu demo program dari internet menggunakan JavaScript yang masih menggunakan topik dari minggu ke-1 hingga praktikum minggu ke-3. (Diperbolehkan membuat program sendiri apabila tidak dapat menemukan di internet). Jelaskan proses program tersebut berjalan berdasarkan pemahaman yang telah kalian pelajari.

2. Jelaskan perbedaan hasil dua baris terakhir dalam program berikut: 
```js 
let a1 = "banana";
let a2 = ("b" + "a" + + "a" + "a").toLowerCase()

console.log(`${a1}`);
console.log(`${a2}`);
```
Bagaimana hasil kedua baris tersebut? Mengapa hasilnya demikian? Jelaskan. Silahkan menggunakan chatGPT namun harus tetap dipahami prosesnya seperti apa.


### Jawaban

1. Di sini saya membuat demo program saya sendiri yang mana untuk materi yang saya gunakan di program ini menggunakan topik minggu ke 1 hingga 3 , untuk kode program seperti ini : 
```js
let nama = prompt("Masukan Namamu ? ");
let age = prompt("Masukan Usia mu ? ");
let asal = prompt("Darimana asal mu?")
const wavingHand = '\u{1F44B}';

message = `${wavingHand} Hi!!! Nama ku ${nama} Umur ku ${age} Tahun , dan asal ku dari ${asal}`

console.log(message)
```

dimana untuk penjelasan nya sendiri yakni :

    1. Pertama, program akan meminta user untuk memasukkan nama dengan fungsi prompt("Masukan Namamu ? "). Hasil input akan disimpan dalam 
    variabel nama.
    
    2. Selanjutnya, program akan meminta user untuk memasukkan usia dengan fungsi prompt("Masukan Usia mu ? "). Hasil input akan disimpan dalam variabel age.
    
    3. Terakhir, program akan meminta user untuk memasukkan asal dengan fungsi prompt("Darimana asal mu?"). Hasil input akan disimpan dalam variabel asal.


Setelah mengambil input dari user, program akan menyimpan emoji waving hand dalam variabel wavingHand menggunakan Unicode escape sequence.

Kemudian, program akan membuat sebuah pesan yang berisi variabel-variabel yang telah diisi oleh user dengan memanfaatkan string literals. Variabel-variabel tersebut diisikan ke dalam pesan dengan template literal ${nama}, ${age}, dan ${asal}.

Setelah itu, program akan menampilkan pesan dengan menampilkan variabel message menggunakan console.log().

Dalam contoh ini, program akan menampilkan sebuah pesan yang mengucapkan "Hi!!! Nama ku (nama), Umur ku (usia) Tahun, dan asal ku dari (asal)" dengan emoji waving hand di depannya.

untuk pengambilan materi nya adalah sebagai berikut :

    1. Penggunaan console.log , materi minggu 1 
    2. Penggunaan Unicode , materi minggu 2
    3. Penggunaan Identifiers dan Reserved Words , materi minggu 2
    4. Penggunaan Template Literals , materi minggu 3
    5. Penggunaan variable let serta const , materi minggu 3

untuk output nya dapat di lihat di screeenshot berikut :

    1. Pengguna di minta untuk memasukan nama , umur , serta asal dengan fungsi prompt 
<img src= "Screenshot (1048).png" width="850">
<img src= "Screenshot (1049).png" width="850">
<img src= "Screenshot (1050).png" width="850">
    
    2. Hasil setelah pengguna menginput nama , umur serta asal dengan fungsi prompt
<img src= "Screenshot (1051).png" width="850">

 
2. Kedua baris tersebut menghasilkan output yang sama karena variabel a1 dan a2 pada dasarnya memiliki nilai yang sama yaitu "banana". Namun, nilai a2 dihasilkan melalui proses yang berbeda dari nilai a1.

    Pada baris kedua, nilai variabel a2 dihasilkan dengan cara menggabungkan beberapa string yaitu "b", "a", "+", "a", dan "a". Perlu diperhatikan bahwa terdapat operator unary plus (+) di antara string "a" yang digunakan untuk memaksa konversi string "a" menjadi nilai number. Namun, karena tidak ada karakter angka sebelum atau sesudah string "a", maka nilai yang dihasilkan dari operasi tersebut adalah NaN (Not a Number).

    Setelah itu, nilai NaN diubah menjadi string dan digabungkan dengan string "b" dan "a" sehingga membentuk string "baNaNa". Kemudian, string tersebut diubah menjadi lowercase dengan menggunakan metode .toLowerCase() sehingga hasil akhirnya adalah "banana".

    Pada baris ketiga dan keempat, nilai variabel a1 dan a2 diprint ke console menggunakan fungsi console.log(). Karena kedua variabel memiliki nilai yang sama yaitu "banana", maka output dari kedua baris tersebut adalah "banana".
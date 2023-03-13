# ASSIGNMENT 1
Nama : Jein Ananda

Nim : 10221031

## Soal 

1. [40 points] Choose four string methods and give some examples how to use them.

2. [40 points] Explain the following code and what the results are
```js 
let a = 1, b = 2, c = 3; console.log(a, b, c);
[a, b, c] = [a, c, b]; console.log(a, b, c);
[a, b, c] = [c ,b, a]; console.log(a, b, c);
[a, b, c] = [a, c, b]; console.log(a, b, c);
[a, b, c] = [c, b, a]; console.log(a, b, c);
[a, b, c] = [a, c, b]; console.log(a, b, c);
```

3. [20 points] Calculate the total annual income of Abdul from the following paragraph. 

“Abdul earns 2.800.000 rupiahs from salary per month, 5.300.000 rupiahs from freelance per month, and 20.300.00 rupiahs per year.”

Hint: define it as a string text and extract the number by the string methods.


### Jawaban 

1. -toUpperCase() , Metode ini mengubah semua karakter dalam string menjadi huruf kapital.
Contoh penggunaan: 
```js let nama = "john doe";
let namaKapital = nama.toUpperCase();
console.log(namaKapital); // Output: "JOHN DOE"
```

- toLowerCase() , Metode ini mengubah semua karakter dalam string menjadi huruf kecil.
Contoh penggunaan:
```js
let kata = "JANGAN MENGELUH";
let kataKecil = kata.toLowerCase();
console.log(kataKecil); // Output: "jangan mengeluh"
```

- charAt , Metode ini mengembalikan karakter pada indeks yang ditentukan dalam string.
Contoh penggunaan:
```js 
let kata = "JavaScript";
let karakter = kata.charAt(4);
console.log(karakter); // Output: "S"
```

- substring() , Metode ini mengembalikan substring dari string, mulai dari indeks awal hingga akhir yang ditentukan.
Contoh penggunaan:
```js 
let kata = "Hello World";
let substring = kata.substring(0, 5);
console.log(substring); // Output: "Hello"
```

2. Kode tersebut menggunakan sintaksis destructuring assignment untuk menukar nilai variabel b dan c pada array. Berikut adalah penjelasan baris per baris dari kode tersebut beserta hasilnya:

let a = 1, b = 2, c = 3; console.log(a, b, c); - Variabel a, b, dan c diinisialisasi dengan nilai 1, 2, dan 3. Kemudian, nilai dari ketiga variabel tersebut dicetak ke konsol. Output yang dihasilkan adalah 1 2 3.

[a, b, c] = [a, c, b]; console.log(a, b, c); - Array [a, c, b] digunakan untuk menginisialisasi ulang nilai dari variabel a, b, dan c. Dalam hal ini, nilai dari variabel b dan c ditukar sehingga variabel b menjadi 3 dan variabel c menjadi 2. Kemudian, nilai dari ketiga variabel tersebut dicetak ke konsol. Output yang dihasilkan adalah 1 3 2.

[a, b, c] = [c ,b, a]; console.log(a, b, c); - Array [c, b, a] digunakan untuk menginisialisasi ulang nilai dari variabel a, b, dan c. Dalam hal ini, nilai dari ketiga variabel ditukar sehingga variabel a menjadi 2, variabel b menjadi 3, dan variabel c menjadi 1. Kemudian, nilai dari ketiga variabel tersebut dicetak ke konsol. Output yang dihasilkan adalah 2 3 1.

[a, b, c] = [a, c, b]; console.log(a, b, c); - Array [a, c, b] digunakan untuk menginisialisasi ulang nilai dari variabel a, b, dan c. Kembali lagi, nilai dari variabel b dan c ditukar sehingga variabel b menjadi 2 dan variabel c menjadi 3. Kemudian, nilai dari ketiga variabel tersebut dicetak ke konsol. Output yang dihasilkan adalah 2 2 3.

[a, b, c] = [c, b, a]; console.log(a, b, c); - Array [c, b, a] digunakan untuk menginisialisasi ulang nilai dari variabel a, b, dan c. Kembali lagi, nilai dari ketiga variabel ditukar sehingga variabel a menjadi 3, variabel b menjadi 2, dan variabel c menjadi 2. Kemudian, nilai dari ketiga variabel tersebut dicetak ke konsol. Output yang dihasilkan adalah 3 2 2.

[a, b, c] = [a, c, b]; console.log(a, b, c); - Array [a, c, b] digunakan untuk menginisialisasi ulang nilai dari variabel a, b, dan c. Kembali lagi, nilai dari variabel b dan c ditukar sehingga variabel b menjadi 2 dan variabel c menjadi 3. Kemudian, nilai dari ketiga variabel tersebut dic

3. Calculate the total annual income of Abdul from the following paragraph. 

“Abdul earns 2.800.000 rupiahs from salary per month, 5.300.000 rupiahs from freelance per month, and 20.300.00 rupiahs per year.” :
```js 
let salaryPerMonth = 2800000;
let freelancePerMonth = 5300000;
let otherAnnualIncome = 20300000;

let totalAnnualIncome = (salaryPerMonth * 12) + (freelancePerMonth * 12) + otherAnnualIncome;

console.log("Total Annual Income of Abdul: " + totalAnnualIncome + " rupiahs");
```
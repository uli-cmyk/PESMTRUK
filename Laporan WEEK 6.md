# Praktikum Week 6 
NAMA : JEIN ANANDA

NIM : 10221031

## Soal
1. [40 points] What kind of situation whether we need to use for loops or while loop? Explain with a concrete example.

2. [40 points] Write a JavaScript program to create the following multiplication table with user input up to number 9:
```js
    1 2 3 
   ------
1 | 1 2 3
2 | 2 4 6
3 | 3 6 9
```

Use prompt-sync to get user input, for loops, and put the correct space when the result of multiplication is two digit numbers.

3. [30 points] To emulate the age restriction of an webpage in a website (figure on the right side), make a simpler one that can ask the user to input their age or cancel to enter the page. The program should stop asking the user input until the user type “cancel” in the program.


### Jawaban

1.) Ketika kita memiliki jumlah iterasi yang pasti dan terbatas, maka lebih baik menggunakan for loop. Namun, jika kita tidak tahu berapa kali iterasi yang dibutuhkan atau perlu melakukan iterasi sampai kondisi tertentu tercapai, maka lebih baik menggunakan while loop.

Sebagai contoh, jika kita ingin mencetak angka dari 1 hingga 10, kita bisa menggunakan for loop:
```js
for i in range(1, 11):
    print(i)
```

Namun, jika kita ingin meminta pengguna untuk memasukkan angka hingga mereka memasukkan angka yang lebih besar dari 10, maka kita perlu menggunakan while loop:
```js
angka = 0
while angka <= 10:
    angka = int(input("Masukkan sebuah angka: "))
```

Dalam contoh di atas, program akan terus meminta pengguna untuk memasukkan angka sampai mereka memasukkan angka yang lebih besar dari 10. Ini tidak mungkin dilakukan dengan for loop karena kita tidak tahu berapa kali pengguna akan memasukkan angka sebelum memasukkan angka yang lebih besar dari 10.

2.) Program dari no 2 adalah :
```js
const prompt = require('prompt-sync')();

// Get user input
const num = parseInt(prompt("Masukkan angka (maksimum 9): "));

// Create table header
let header = "  ";
for (let i = 1; i <= num; i++) {
  header += i + " ";
}
console.log(header);

// Create table border
let border = "--";
for (let i = 1; i <= num; i++) {
  border += "--";
}
console.log(border);

// Create table body
for (let i = 1; i <= num; i++) {
  let row = i + " |";
  for (let j = 1; j <= num; j++) {
    let result = i * j;
    if (result < 10) {
      row += " " + result + " ";
    } else {
      row += result + " ";
    }
  }
  console.log(row);
}
```

dengan contoh output : 

<img src="SOAL NO 2.png">

3.) di sini saya menggunakan HTML,CSS,JS sebagai pengimplementasian program nya , untuk kode program nya sebagai berikut

HTML :
```HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Week 6</title>
    <link rel="stylesheet" href="WEEK 6 .CSS">
</head>
<body>
    <div id="container">
      <div id="title">ENTER</div>
      <div id="state">Entry will be granted only to those who are older than 18</div>
      <div id="ageForm">
        <input type="text" id="oldness" placeholder="Enter Your Age">
        <button id="submit">Submit</button>
        <button id="cancel">Cancel</button>
      </div>
      <p id="entry"></p>
    </div>
    <script src="WEEK 6.JS"></script>
    </body>
    </html>
  </body>
  </html>
  ```

  CSS : 
  ```CSS
  @import url('https://fonts.googleapis.com/css?family=Poller+One|ZCOOL+XiaoWei&display=swap');

* {
  padding: 0;
  margin: 0;
  font-family: 'ZCOOL XiaoWei', serif;
}

body {
    position: relative;
    width: 100%;
    height: 100vh;
    background: url(744908.jpg);
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
}
#container {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#title {
  text-align: center;
  font-size: 6rem;
  font-family: 'Poller One', cursive;
  letter-spacing: 2.2rem;
  color: #ffffff;
  padding-top: 3rem;
  padding-bottom: 1rem;
}

#title:hover {
  letter-spacing: 4.5rem;
  transition: all 1.5s ease-out; 
}


input { 
padding: .6rem;
font-size: 1rem;
}

button {
  padding: .6rem;
  margin-top: 1.5rem;
  margin-left: .4rem;
  font-size: 1rem;
  background-color: #ffffff;
  color: #1E1F26;
  font-family: 'Poller One', cursive;
  font-weight: 400;
  letter-spacing: .2rem;
  border: 1px solid #1E1F26;
  transition: all 3s ease-out;
}

button:hover {
  background-color: white;
}


#ageForm {
  margin: 0 auto;
  position: relative;
  text-align: center;
  padding-bottom: 2rem;
}

#state {
  text-align: center;
  font-size: 1.2rem;
}

#entry {
  font-size: 1.8rem;
  text-align: center;
}
```

JAVASCRIPT : 
```js
const checkAge = () => {
    let ageInput = parseInt(document.querySelector('#oldness').value);
    const entryGranted =  document.querySelector("#entry");
  
    if (isNaN(ageInput)) {
      entryGranted.innerHTML = "Please enter a valid age.";
    } else if (ageInput >= 18 && ageInput <= 90) {
      entryGranted.innerHTML = "You May Enter";
    } else if (ageInput >= 13 && ageInput <= 17) {
      entryGranted.innerHTML = "You Shall Not Pass!";
    } else {
      entryGranted.innerHTML = "Shouldn't you be in bed by now?";
    }
  }
  
  const submitButton = document.querySelector("#submit");
  const cancelButton = document.querySelector("#cancel");
  
  submitButton.addEventListener("click", () => {
    checkAge();
  });
  
  cancelButton.addEventListener("click", () => {
    const ageInput = document.querySelector("#oldness");
    const entryGranted =  document.querySelector("#entry");
    ageInput.value = "";
    entryGranted.innerHTML = "";
  });
  ```

  Program akan berjalan seperti ini :

    1. User akan di minta untuk menginput umur 
<img src="Screenshot (1119).png">

    2. Setelah User menginput umur , user dapat mengclick button Submit , jika umur >= 18 maka output program " You May Enter " namun jika umur 
    >=13 && <=17 maka output program "You Shall Not Pass!" , sedangkan jika umur <13 output program "Shouldn't you be in bed by now?"

<img src="Screenshot (1120).png">
<img src="Screenshot (1121).png">
<img src="Screenshot (1122).png">
    
    3. dan jika user mengclick button cancel akan muncul output " Acess Denied "

<img src="Screenshot (1124).png">
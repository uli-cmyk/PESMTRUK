# Praktikum Week 9 
Nama : Jein Ananda

Nim : 10221031 

## Soal

1. [30 poin] Sebutkan 3 kegiatan yang kalian lakukan sehari-hari yang dapat diubah menjadi suatu fungsi. Implementasi fungsi tersebut kedalam   JavaScript. Berikan juga contoh penggunaannya.

Berikut contoh salah satu kegiatan yang mungkin.

```js
// Berikut adalah fungsi untuk menggambarkan kegiatan makan
function angkatSendok(n) {
  for (let i = 0; i < n; i++>) {
    console.log(`menangangkat sendork yang ke-${i+1} kali`);
  }
}

angkatSendok(4);

```

2. [70 poin] Buatlah suatu fungsi untuk mengkonversi suatu bilangan ke bentuk string yang merupakan pembacaan bilangan tersebut:

    1, menjadi 'satu',
    2, menjadi 'dua',
    3, menjadi 'tiga',
    4, menjadi 'empat',
    5, menjadi 'lima',
    dst.
    Fungsi yang akan kalian buat tersebut harus mampu mengkonversi hingga bilangan ke-100.

### Jawaban

1. Saya membuat 3 fungsi ada Fungsi untuk menyalakan lampu, Fungsi untuk mengirim pesan teks, dan Menghitung Luas Lingkaran
```js
// Fungsi menyalakan lampu 

function switchOnLight(n) {
    for (let i = 0; i < n ; i++){
        console.log("Lampu dinyalakan.");
    }
}

switchOnLight(3)


// Mengirim Pesan Teks

function sendMessage(message) {
    for (let i = 0; i < message ; i++) {
        sendMessage("Halo, apa kabar?"); // Memanggil fungsi sendMessage() 2 kali
            console.log(`Pesan yang terkirim: ${message}`);
    }
}

sendMessage(2)

// Menghitung jari-jari

function hitungLuasLingkaran(jariJari) {
    const pi = 3.14;
    for (let i = 1; i <= jariJari; i++) {
      const jari = i;
      const luas = pi * jari * jari;
      console.log(`Luas lingkaran dengan jari-jari ${jari} adalah ${luas}`);
    }
  }
  
  hitungLuasLingkaran(2);
```

berikut output nya : 

<img src = "Screenshot (1205).png" >


2. 
```js
function konversiAngkaKeString(angka) {
    if (angka === 0) {
      return "nol";
    } else if (angka < 0 || angka > 100) {
      return "input tidak valid";
    } else {
      let satuan = ["", "satu", "dua", "tiga", "empat", "lima", "enam", "tujuh", "delapan", "sembilan", "sepuluh", "sebelas"];
      if (angka < 12) {
        return satuan[angka];
      } else if (angka < 20) {
        return satuan[angka - 10] + " belas";
      } else if (angka < 100) {
        return satuan[Math.floor(angka / 10)] + " puluh " + satuan[angka % 10];
      } else {
        return "seratus";
      }
    }
  }
  
  console.log(konversiAngkaKeString(0)); // nol
  console.log(konversiAngkaKeString(7)); // tujuh
  console.log(konversiAngkaKeString(11)); // sebelas
  console.log(konversiAngkaKeString(19)); // sembilan belas
  console.log(konversiAngkaKeString(25)); // dua puluh lima
  console.log(konversiAngkaKeString(89)); // delapan puluh sembilan
  console.log(konversiAngkaKeString(100)); // seratus
  console.log(konversiAngkaKeString(101)); // input tidak valid
```

berikut output nya :

<img src="Screenshot (1206).png">
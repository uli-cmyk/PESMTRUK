# Exercise 08

Nama : Jein Ananda

Nim : 10221031

## Soal

1. [30 poin] Pilih dan telusuri satu Web APIs di daftar yang ada di MDN Web Docs. Berikan salah satu contoh penggunaan yang berhubungan langsung dengan permasalahan organisasi atau manajemen.

2. [70 poin] Berikut ini diberikan data last access LMS ITK untuk mahasiswa Sistem Informasi yang mengikuti mata kuliah Pemrograman Terstruktur. Data dapat diunduh di 20230426-1505WITA-last-access.json. Menggunakan regular expression, seleksi setiap baris untuk mendapatkan jam dan menit. Menggunakan nama file yang diberikan, tentukan waktu terakhir (tanggal dan jam LMS diakses oleh mahasiswa). Perhitungan waktu bisa menggunakan library Dates and Times.

### Jawaban

1. Salah satu Web API yang dapat digunakan untuk permasalahan organisasi atau manajemen adalah Web Storage API. Web Storage API menyediakan cara untuk menyimpan data di sisi klien (browser) secara persisten.

    Contoh penggunaan yang berhubungan langsung dengan permasalahan organisasi atau manajemen adalah untuk menyimpan preferensi pengguna atau pengaturan dalam aplikasi web. Misalnya, dalam sebuah aplikasi manajemen proyek, pengguna dapat mengatur preferensi tampilan seperti tema warna, ukuran teks, atau tata letak.

    Dengan menggunakan Web Storage API, preferensi tersebut dapat disimpan di sisi klien sehingga saat pengguna membuka kembali aplikasi, preferensi yang disimpan sebelumnya dapat diambil dan diterapkan secara otomatis. Hal ini memungkinkan pengguna memiliki pengalaman yang konsisten dan sesuai dengan preferensinya setiap kali menggunakan aplikasi.

2. Berikut kode program serta penjelasan nya 
```js 
const data = `18 hours 17 mins
Never
17 hours 17 mins 
14 days 1 hour 
13 hours 6 mins 
15 days 6 hours 
15 days 7 hours 
14 days 15 hours 
57 days 6 hours
1 hour 40 mins
8 days 5 hours 
15 days 4 hours 
5 hours 5 mins
4 hours 39 mins 
19 hours 56 mins 
17 hours 30 mins
40 days 18 hours
19 hours 34 mins 
8 days 5 hours
6 hours 55 mins 
7 days 17 hours 
6 days 14 hours 
4 mins 40 secs 
20 hours 37 mins 
8 days 5 hours
3 hours 52 mins 
5 days 18 hours 
6 hours 40 mins 
8 days 15 hours 
8 days 4 hours
1 hour 36 mins
2 hours 19 mins 
18 days 14 hours 
8 days 6 hours
7 hours
6 days 14 hours
8 days 6 hours
7 hours 14 mins 
6 days 16 hours 
17 hours 51 mins 
7 hours 5 mins
6 days 14 hours 
7 days 5 hours
6 days 13 hours
1 hour 32 mins`;

// Mencocokkan jam dan menit menggunakan regular expression
const regex = /(\d+)\s(hours?|mins?)/g;
const matches = data.match(regex);

// Menghitung waktu terakhir dengan menggunakan Dates and Times library
const now = new Date();
let lastAccess = null;

for (let i = 0; i < matches.length; i++) {
  const match = matches[i];
  const [time, unit] = match.split(' ');
  const duration = unit.startsWith('hour') ? 'hours' : 'minutes';

  const date = new Date(now.getTime());
  if (duration === 'hours') {
    date.setHours(now.getHours() - parseInt(time));
  } else {
    date.setMinutes(now.getMinutes() - parseInt(time));
  }

  if (!lastAccess || date > lastAccess) {
    lastAccess = date;
  }
}

console.log('Waktu terakhir LMS diakses oleh mahasiswa:', lastAccess);
```

Dalam contoh di atas, pertama-tama, data yang diberikan disimpan dalam variabel data. Kemudian, dilakukan pencocokan menggunakan regular expression untuk mencocokkan setiap baris yang berisi jam dan menit. Hasil pencocokan disimpan dalam array matches.

Selanjutnya, menggunakan library Dates and Times (misalnya, moment.js atau JavaScript built-in Date), waktu terakhir dihitung dengan melakukan iterasi melalui array matches. Untuk setiap cocokan, waktu sekarang (now) dikurangi dengan jumlah jam atau menit yang ditemukan. Kemudian, dilakukan perbandingan untuk menentukan waktu terakhir yang terbaru.

Akhirnya, waktu terakhir diakses LMS oleh mahasiswa ditampilkan dalam konsol. Harap perhatikan bahwa implementasi ini tidak memperhitungkan tanggal yang spesifik, hanya menghitung selisih waktu relatif dari waktu sekarang. Jika Anda perlu memperhitungkan tanggal yang spesifik, lebih baik menggunakan library seperti moment.js untuk manipulasi tanggal dengan lebih mudah.

dan output program nya akan seperti ini = " Waktu terakhir LMS diakses oleh mahasiswa: 2023-05-10T13:36:59.547Z " 
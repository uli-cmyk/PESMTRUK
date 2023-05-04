# Assignment 03

Nama : Jein Ananda

Nim : 10221031

## Soal 

1. [50 points] Explore and explain about the application of JavaScript function to the organizational issues. Organization issues can range across:
data management, 
automation, 
customer relationship management, 
inventory management
financial analysis
You can choose one of the above issues, or a new finding from the internet. Maximum answer is 1000 words.

2. [50 points] Given a shuffled a deck of card (without a joker / 52-card deck), make a JavaScript function that has an input a shuffled deck and give the output of ordered deck. Store the deck of card as an array of string.

### Jawaban 

1. Dengan menggunakan JavaScript untuk membuat skrip pengujian, mudah untuk melakukan Pengujian UI otomatis untuk aplikasi. Ini sangat berguna ketika siklus pengembangan pendek dan fitur harus ditambahkan setiap beberapa minggu untuk memenuhi permintaan pengguna. Selenium sangat direkomendasikan karena fleksibilitas yang ditawarkannya

2. 
```js
const suits = ["Spades", "Diamonds", "Club", "Heart"];
const values = [
  "Ace",
  "2",
  "3",
  "4",
  "5",
  "6",
  "7",
  "8",
  "9",
  "10",
  "Jack",
  "Queen",
  "King",
];

// function to order the deck
function orderDeck(deck) {
  // create an empty array to contain the ordered deck
  const orderedDeck = [];

  // loop through each suit and value to create the ordered deck
  for (let i = 0; i < suits.length; i++) {
    for (let x = 0; x < values.length; x++) {
      let card = { Value: values[x], Suit: suits[i] };
      orderedDeck.push(card);
    }
  }

  // loop through each card in the input deck and find its index in the ordered deck
  for (let i = 0; i < deck.length; i++) {
    let index = orderedDeck.findIndex(
      (card) => card.Value === deck[i].Value && card.Suit === deck[i].Suit
    );

    // remove the card from the ordered deck and add it back in at the correct index
    let card = orderedDeck.splice(index, 1)[0];
    orderedDeck.splice(i, 0, card);
  }

  // return the ordered deck
  return orderedDeck;
}

// create a shuffled deck
let deck = [];
for (let i = 0; i < suits.length; i++) {
  for (let x = 0; x < values.length; x++) {
    let card = { Value: values[x], Suit: suits[i] };
    deck.push(card);
  }
}
for (let i = deck.length - 1; i > 0; i--) {
  let j = Math.floor(Math.random() * i);
  let temp = deck[i];
  deck[i] = deck[j];
  deck[j] = temp;
}

console.log("The shuffled deck is:");
console.log(deck);

// order the deck
let orderedDeck = orderDeck(deck);

console.log("The ordered deck is:");
console.log(orderedDeck);
```

orderDeck menerima sebuah array dari objek yang merepresentasikan setumpuk kartu yang telah diacak, dan mengembalikan sebuah array dari objek yang merepresentasikan setumpuk kartu yang terurut. Fungsi ini dilakukan dengan membuat sebuah array kosong baru bernama orderedDeck dan menambahkan setiap kartu secara berurutan, kemudian melakukan looping melalui setiap kartu pada setumpuk kartu yang diinputkan dan mencari indeksnya pada setumpuk kartu yang telah diurutkan. Setelah itu, fungsi ini akan menghapus kartu tersebut dari setumpuk kartu yang telah diurutkan dan menambahkannya kembali pada indeks yang tepat. Akhirnya, fungsi ini mengembalikan setumpuk kartu yang telah diurutkan.
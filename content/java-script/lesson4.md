# # Podstawy Java Script — Lekcja 4 — Funkcje

```jsx
const product = 'Król Kiżuczy'
let price = 20
console.log(product, price)
// Wynik: "Król Kiżuczy", 20

price = 10
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 20
```

<br>

* [JavaScript Math.random()](https://www.w3schools.com/js/js_random.asp)

<br>

```jsx
const product = 'Król Kiżuczy'
let price = 20
console.log(product, price)
// Wynik: "Król Kiżuczy", 20

price = Math.floor(Math.random() * 20 + 1);
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 1-20
```

```jsx
const product = 'Król Kiżuczy'
let price = 20
console.log(product, price)
// Wynik: "Król Kiżuczy", 20

const maxValue = 20
price = Math.floor(Math.random() * maxValue + 1);
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 1-20
```

```jsx
const randomNumber = Math.floor(Math.random() * 100 + 1);
// przykładowa wartość dla randomNumber: 41
const price1 = randomNumber
const price2 = randomNumber
console.log('cena 1 ', price1)
// Wynik: "cena 1", 41
console.log('cena 2 ', price2)
// Wynik: "cena 2", 41
```

```jsx
function random_number() {
    return Math.floor(Math.random() * 100 + 1);
};

const product = 'Król Kiżuczy'
let price = random_number()
console.log(product, price)
// Wynik: "Król Kiżuczy", 1-100

price = random_number()
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 1-100
```

```jsx
function random_number(max) {
    return Math.floor(Math.random() * max + 1);
};

const product = 'Król Kiżuczy'
let price = random_number(100)
console.log(product, price)
// Wynik: "Król Kiżuczy", 1-100

price = random_number(10)
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 1-10
```

```jsx
function random_number(min, max) {
    return Math.floor(Math.random() * (max - min) + min);
};

const product = 'Król Kiżuczy'
let price = random_number(51, 100)
console.log(product, price)
// Wynik: "Król Kiżuczy", 51-100

price = random_number(1, 50)
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 1-50
```

```jsx
const datas = ['pies', 'kot', 'ryba', 'rower', {author: 'Mickiewicz Adam', title: 'Pan Tadeusz'}]

function get_random_value_from_array(arr) {
    return arr[Math.floor(Math.random() * arr.length)]
}

console.log(get_random_value_from_array(datas))
// Wynik: Losowy element z tablicy
console.log(datas[Math.floor(Math.random() * datas.length)])
```

### [Powrót do strony głównej](../../README.md)
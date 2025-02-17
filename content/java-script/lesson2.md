# Podstawy Java Script — Lekcja 2 — Poruszanie się po obiektach i tablicach

## Poruszanie się po obiektach i tablicach — ćwiczenia z logowaniem

<br>

* Przy pomocy darmowych generatorów json tworzymy i kopiujemy obiekt:
  * [https://json-generator.com/](https://json-generator.com/)
  * [https://www.jsongenerator.io/](https://www.jsongenerator.io/)

```jsx
const person = {
    "_id": "6745f1ea2c3654be1f918772",
    "index": 0,
    "guid": "ab817966-232e-49cc-9535-b29e74f1d42e",
    "isActive": false,
    "balance": "$3,903.26",
    "picture": "http://placehold.it/32x32",
    "age": 37,
    "eyeColor": "green",
    "name": "Juliana Blake",
    "gender": "female",
    "company": "ONTAGENE",
    "email": "julianablake@ontagene.com",
    "phone": "+1 (848) 485-2607",
    "address": "160 Harbor Lane, Alfarata, Marshall Islands, 7071",
    "about": "Consequat aliquip sit reprehenderit dolore culpa Lorem ea qui. Dolor occaecat elit tempor laboris laborum.",
    "registered": "2014-06-30T01:31:58 -02:00",
    "latitude": 38.692913,
    "longitude": -45.931596,
    "tags": [
        "excepteur",
        "ut",
        "exercitation",
        "fugiat",
        "consectetur",
        "esse",
        "eu"
    ],
    "friends": [
        {
            "id": 0,
            "name": "Porter Blackwell"
        },
        {
            "id": 1,
            "name": "Laverne Klein"
        },
        {
            "id": 2,
            "name": "Shelia Munoz"
        }
    ],
    "greeting": "Hello, Juliana Blake! You have 3 unread messages.",
    "favoriteFruit": "banana"
}
```

<br>

* Przy pomocy ```console.log(person)``` otrzymamy cały obiekt z wszystkimi informacjami.
* Co robić, gdy chcemy dotrzeć tylko do pojedynczych informacji?

```jsx
console.log(person.name)
// Wynik: "Juliana Blake"

console.log(person.gender)
// Wynik: "female"

console.log(person.email)
// Wynik: "julianablake@ontagene.com"
```

<br>

* Gdy będziemy próbować się dostać do ```person.tags``` to wylogujemy całą tablicę
* Numerowanie elementów tablicy zaczyna się o 0 (zero)
* Więc string ```"exercitation"``` mimo iż jest to trzeci (3) element tablicy to jego numer index to 2

```jsx
console.log(person.tags)
/* Wynik: (7) ["excepteur", "ut", "exercitation", "fugiat", "consectetur", …]
0: "excepteur"
1: "ut"
2: "exercitation"
3: "fugiat"
4: "consectetur"
5: "esse"
6: "eu"
*/
```

<br>

* Żeby wylogować string ```"exercitation"``` musimy:

<br>

```jsx
console.log(person.tags[2])
// Wynik: "exercitation"
```
<br>

* Druga tablica w obiekcie  ```person``` to ```fiends```
* Na tej tablicy znajdują się obiekty

<br>

```jsx
console.log(person.friends[1])
// Wynik: {id: 1, name: "Laverne Klein"}

console.log(person.friends[1].name)
// Wynik: "Laverne Klein"
```

<br>

* Jeśli na tablicy będziemy szukać po nie istniejącym numerze index

<br>

```jsx
console.log(person.friends[100])
// Wynik: undefined

console.log(person.friends[100].name)
// Wynik: TypeError: Cannot read properties of undefined (reading 'name')
```

### Następny rozdział: [Podstawy Java Script — Lekcja 3 — Nazwy zastrzeżone](lesson3.md)

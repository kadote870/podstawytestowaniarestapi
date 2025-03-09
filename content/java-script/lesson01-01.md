# Podstawy Java Script — Lekcja 1 — Typy zmiennych

> 💡 Podczas ćwiczeń z postman można użyć [Postman Echo](https://learning.postman.com/docs/developer/echo-api/) -
```https://postman-echo.com/get```

* Java Script pierwotnie został stworzony na potrzeby tworzenia bardziej skomplikowanych stron internetowych, jednak
  przez prostotę i elastyczność zaczęto znajdywać dla niego również inne zastosowania np. backend — Node.JS.
* Z racji tego, że pierwsza wersja JS została stworzona w zaledwie kilka tygodni, to trzeba mieć na uwadze to, że czasem
  jego logika — a właściwie jej brak — może czasami zaskakiwać.

## Ćwiczenia z konsolą I

* Znak: ```/``` - ukośnik, prawy ukośnik (_slash_, _forward slash_).
* Podwójny ```//``` - Umożliwia nam wyłączenie danego fragmentu kodu. Kod nie będzie wykonywany.
* Stosując ```//``` możemy też umieścić w kodzie jakiś komentarz.
* Podobne działanie ma również zastosowanie konstrukcji ```/*```{KOD LUB TEKST}```*/```.

<br>

```jsx
console.log('Hello world!')
// Wynik: "Hello world!"
```

```jsx
console.log(4)
// Wynik: 4
```

```jsx
console.log(2 + 2)
// Wynik: 4
```

```jsx
console.log(2 + 2 * 2)
// Wynik: 6
```

```jsx
console.log((2 + 2) * 2)
// Wynik: 8
```

```jsx
console.log({a: 2, b: 2, c: "d", e: ["g", "h", "j", "k"]})
/*
Wynik:
{
a:2,
b:2,
c:"d",
e:[
    "g",
    "h",
    "j",
    "k"
   ]
}
*/
```

## [Arkana szaleństwa w Java Script](lesson01-02.md)

---

## Ćwiczenia z konsolą II — zmienne, deklarowanie zmiennych

```jsx
var a = 'Hello world!'
console.log(a)
// Wynik: "Hello world!"
```

```jsx
var a = 4
console.log(a)
// Wynik: 4
```

```jsx
var a = 2 + 2
console.log(a)
// Wynik: 4
```

```jsx
var a = 2 + 2 * 2
console.log(a)
// Wynik: 6
```

```jsx
var a = (2 + 2) * 2
console.log(a)
// Wynik: 8
```

```jsx
console.log({a: 2, b: 2, c: "d", e: ["g", "h", "j", "k"]})
console.log(a)
/*
Wynik:
{
a:2,
b:2,
c:"d",
e:[
    "g",
    "h",
    "j",
    "k"
   ]
}
*/
```

## Ćwiczenia z konsolą III — zmienne, deklarowanie zmiennych

```jsx
var a = 4
var b = 2
console.log(a + b)
// Wynik: 4

console.log(a - b)
// Wynik: 2

console.log(b + b)
// Wynik: 4

console.log(b + b * a)
// Wynik: 10

console.log((b + b) * a)
// Wynik: 16
```

## Ćwiczenia z konsolą IV — zmienna var i const

* W początkowym okresie JS posiadał tylko jeden typ zmiennej ```var```
* Z czasem wprowadzono dwie nowe ```const``` i ```let``` - ich działanie jest znacznie bardziej przewidywalne
* Obecnie nie używa się stosuje zmiennej ```var``` jednak do dziś jest ona wspierana — istnieje prawdopodobieństwo, że
  bez niej spora część internetu przestałaby działać poprawnie

<br>

```jsx
var product = 'Rubaszny Krasnolud'
console.log(product)
// Wynik: "Rubaszny Krasnolud"
```

<br>

* Poniżej możemy zauważyć, że kod wykonuje się linia po linii od góry do dołu.
* Pojawia się problem, najpierw logujemy zmienną ```product```, która jest pusta dlatego wynik to ```undefined```
* Problem polega na tym, że kod programu wykonuje się do końca.

<br>

```jsx
console.log(product)
var product = 'Rubaszny Krasnolud'
// Wynik: undefined
```

<br>

* Zacznijmy używać zmiennej ```const```, jest ona bardziej eleganckim rozwiązaniem.
* Zmienną ```const``` charakteryzuje to, że jest o zmienna, która jest niezmienna — masło maślane — ale najlepiej to
  omawia jej intencję jej powstania.
* Jest to zmienna, dla której wartość możemy przypisać tylko raz.

<br>

```jsx
const product = 'Rubaszny Krasnolud'
console.log(product)
// Wynik: "Rubaszny Krasnolud"
```

<br>

* Poniżej widzimy przykład wywołania zmiennej ```const``` przed przypisaniem do jej wartości
* Podczas próby wykonania programu, program przestaje się wykonywać i dostajemy w konsoli błąd

<br>

```jsx
console.log(product)
const product = 'Rubaszny Krasnolud'
// Wynik: ReferenceError: Cannot access 'product' before initialization
```

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product)
// Wynik: "Rubaszny Krasnolud"
```

## Ćwiczenia z konsolą V — logowanie dwóch zmiennych

<br>

* Dwie zmienne obok siebie wywołują błąd
* Ponadto edytor kodu już na tym etapie powinien wyświetlić informacje o błędzie

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product
price
)
// Wynik: SyntaxError: missing ) after argument list
```

<br>

* Pomiędzy dwiema zmiennymi umieszczamy znak ```+```
* Finalnie obie tworzą jeden napis (string)

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product + price)
// Wynik: "Rubaszny Krasnolud20"
```

<br>

* Pomiędzy dwiema zmiennymi umieszczamy znak ```,``` (przecinek)
* Obie zmienne zostają wylogowane osobno z zachowaniem ich typów — osobno napis (string) i osobna liczba

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product, price)
// Wynik: "Rubaszny Krasnolud", 20
```

## Ćwiczenia z konsolą V — promocja w sklepie — zmienna let

* Załóżmy sobie scenariusz, że będziemy logować w konsoli status produktu, który trafi na promocję.
* Oczywiście dostaniemy błąd, jak wcześniej zauważyliśmy zmienna ```const``` jest bardziej eleganckim rozwiązaniem.
* Nie możemy stworzyć dwóch zmiennych o takiej samej nazwie
* Przy zmiennej ```var``` nie byłoby takich problemów

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product, price)

const price = 10
console.log('Promocja: ', product, price)
// Wynik: SyntaxError: Identifier 'price' has already been declared
```

<br>

* Skoro nie może być dwóch zmiennych o tej samej nazwie, to usuńmy deklarację i spróbujmy przypisać zmiennej ```price```
  nową wartość
* ```price = 10```
* Otrzymujemy błąd, nie możemy przypisać nowej wartości do zmiennej ```const```
* Przy zmiennej ```var``` nie byłoby takich problemów

<br>

```jsx
const product = 'Rubaszny Krasnolud'
const price = 20
console.log(product, price)

price = 10
console.log('Promocja: ', product, price)
// Wynik: TypeError: Assignment to constant variable.
```

<br>

* Zastępujemy deklarację ceny z ```const``` na ```let```
* Teraz program się wykonuje
* Najpierw logujemy informacje o produkcie
* Następnie zmienna ```price``` otrzymuje nową wartość
* Znowu logujemy te same zmienne, ale z nową ceną

<br>

```jsx
const product = 'Rubaszny Krasnolud'
let price = 20
console.log(product, price)
// Wynik: "Rubaszny Krasnolud", 20

price = 10
console.log('Promocja: ', product, price)
// Wynik: "Promocja", "Rubaszny Krasnolud", 10
```

<br>

* Żeby utwierdzić się w przekonaniu, że nasz kod działa dobrze to zmieniamy samą nazwę produktu
* Program działa bez problemów
* Nowa nazwa produktu wyświetla się poprawnie

<br>

```jsx
const product = 'Król Kiżuczy'
let price = 20
console.log(product, price)
// Wynik: "Król Kiżuczy", 20

price = 10
console.log('Promocja: ', product, price)
// Wynik: "Król Kiżuczy", 20
```

### ⏭️ Następny rozdział: [Podstawy Java Script — Lekcja 2 — Poruszanie się po obiektach i tablicach](lesson02.md)

{{ site.data.element.license }}
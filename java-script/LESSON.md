# Podstawy Java Script

## Ćwiczenia z konsolą I
* Znak: ```/``` - ukośnik, prawy ukośnik (_slash_, _forward slash_)
* Podwójny ```//``` - Umożliwia nam wyłączenie danego fragmentu kodu. Kod nie będzie wykonywany.
* Stosując ```//``` możemy też umieścić w kodzie jakiś komentarz.
* Podobne działanie ma również zastosowanie konstrukcji ```/*```{KOD LUB TEKST}```*/```.
---
```jsx
console.log('Hello world!')
// Wynik: Hello world!
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
console.log({ a: 2, b: 2, c: "d", e: ["g", "h", "j", "k"] })
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
---
## Ćwiczenia z konsolą II — zmienne, deklarowanie zmiennych
```jsx
var a = 'Hello world!'
console.log(a)
// Wynik: Hello world!
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
console.log({ a: 2, b: 2, c: "d", e: ["g", "h", "j", "k"] })
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
---
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
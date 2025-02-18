# Podstawy Java Script — Lekcja 3 — Nazwy zastrzeżone

> 💡 Podczas ćwiczeń z postman można użyć [Postman Echo](https://learning.postman.com/docs/developer/echo-api/) -
```https://postman-echo.com/get```

* Zmienne tworzymy używając kluczowych słów:
    * ```var``` — tego nie używajmy, stare mało eleganckie i powoduje problemy
    * ```const``` — to już coś dla prawdziwych Dam i Dżentelmenów — pamiętajmy, że jej wartość możemy zadeklarować tylko
      raz
    * ```let``` — również jest oznaką cywilizacji w Java Script, w tym typie już możemy zmieniać wartość, gdy kod jest
      wykonywany

<br>

* Zmienną deklarujemy w przykładowy sposób ```const a = 10```
    * Mamy zmienną typu ```const```
    * Jej nazwa to ```a```
    * Jej wartość to ```10```
    * Aby ją wywołać w kodzie np. konsoli, podajemy jej nazwę czyli ```a```

<br>

* Nazwy zmiennych w stylu ```a```, ```b```, ```c```, ```d```, ```dupa```, ```dupa1```, ```dupa123``` to nie jest dobrą
  praktyką
* Nazwy w łatwy sposób muszą identyfikować i reprezentować ich zawartość lepszym pomysłem będzie pisanie całych słów lub
  zlepków kilku wyrazów (pamiętajmy o istnieniu notacji np. camelCase, snake_case itd.):
    * ```productName```
    * ```engineType```
    * ```price```
    * ```color```
    * ```serialNumber```
    * ```customerNumber```

<br>

* słowo ```const``` jest potrzebne do zadeklarowania zmiennej, tak więc nie możemy zrobić zmiennej np. ```const let```
* Istnieją również także słowa, które wywołują działanie pewnych mechanizmów wbudowanych w Java Script np. ```console```
  lub ```function```

<br>

```jsx
const const = 'zmienna'
// Wynik: SyntaxError: Unexpected token 'const'

const let = 'zmienna'
// Wynik: SyntaxError: let is disallowed as a lexically bound name

let console = 'zmienna'
console.log(console)
// Wynik: TypeError: console.log is not a function

let function = 'zmienna'
// Wynik: SyntaxError: Unexpected token 'function'
```

### Następny rozdział: [Podstawy Java Script — Lekcja 4 — Funkcje](lesson4.md)
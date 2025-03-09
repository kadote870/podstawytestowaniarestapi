# Funkcje JavaScript

* Zwróć losowy number

```js
function random_number(min, max) {
    return Math.floor(Math.random() * (max - min) + min);
}

const randomNumber = random_number(1, 10);
console.log(randomNumber);
```

* Zwróć losowy boolean (true/false)

```js
function random_boolean() {
    return Boolean(Math.round(Math.random()));
}
```

{{ site.data.element.license }}
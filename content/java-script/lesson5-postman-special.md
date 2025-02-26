# Podstawy Java Script — Lekcja 5 — Postman Special

```js
console.log(pm)
// Wynik: {test: "[Function]"}
```
    
```js
console.log(pm)
// Wynik: {test: "[Function]"}

const pm = 'test'
console.log(pm)
// Wynik: ReferenceError: Cannot access 'pm' before initialization
```

```js
console.log(pm)
// Wynik: {test: "[Function]"}

let pm = 'test'
console.log(pm)
// Wynik: ReferenceError: Cannot access 'pm' before initialization
```

```js
console.log(pm)
// Wynik: {test: "[Function]"}

pm = 'test'
console.log(pm)
// Wynik: test
```

```js
console.log(pm.response)
// Wynik: {id: "08af9357-7c23-487a-8674-2fa0559bdb20", status: "OK", code: 200…}

console.log(pm.response.code)
// Wynik: 200, 400 etc. 

console.log(pm.globals)
// Wynik: {id: "globals/cfe07f57-3062-466c-8802-dd314679e1a8/eb3dee36-17d1-440f-8904-ff5d6e8d646b", mutations: {…}, values: [8]}

console.log(pm.enviorment)
// Wynik: {id: "environment/695a2edb-a974-4311-bfba-230e8ba35239/eb3dee36-17d1-440f-8904-ff5d6e8d646b", name: "trello_prod", mutations: {…}…}

console.log(pm.enviorment.name)
// Wynik: your_env_name || undefined
```


```js
const response = pm.response.json()

console.log(response)
// Wynik: {"exampleResponseBodyKey": "exampleResponseBodyValue"}
```

```js
const response = pm.response.json()

console.log(response.exampleResponseBodyKey)
// Wynik: exampleResponseBodyValue
```


```js
const response = pm.response.json()

pm.globals.set('exampleGlobalVariable', response.exampleResponseBodyKey)

console.log(pm.globals.get('exampleGlobalVariable'))
// Wynik: exampleResponseBodyValue
```


```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```


```js
pm.test("Your test name", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.value).to.eql(100);
});
```

### ⏭️ [Powrót do strony głównej](../../README.md)
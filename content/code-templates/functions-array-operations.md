# Funkcje - Operacje na tablicach

* Filtrowanie tablicy obiektów na podstawie warunku

```js
const objects = []

for (const element of response) {
    if (element.value === condition) {
        objects.push(element);
    }
}

console.log(objects);
```

* Pobieranie losowej wartości z tablicy

```js
function get_random_value_from_array(arr) {
    return arr[Math.floor(Math.random() * arr.length)];
}

const randomValueFromArray = get_random_value_from_array(arr);
console.log(randomValueFromArray);
```

* Usuń duplikaty z tablicy

```js
const arrayWithDuplicates = [1, 2, 3, 4, 4, 5, 5, 6];
const uniqueArray = [...new Set(arrayWithDuplicates)];
console.log(uniqueArray); // Output: [1, 2, 3, 4, 5, 6]
```

* Usuń wskazany element z tablicy

```js
function remove_item_from_array(arr, keyToRemove) {
    const index = arr.indexOf(keyToRemove);
    if (index !== -1) {
        arr.splice(index, 1);
    }
    return arr;
}
```

* znajdź na tablicy obiekt na podstawie wartości i klucza

```js
function find_object_in_array(arr, searchByKey, valueStoredInKey) {
    return arr.find((obj) => obj[searchByKey] === valueStoredInKey);
}

const specificObjectFromArray = find_object_in_array(
    arr,
    searchByKey,
    valueStoredInKey
);
console.log(specificObjectFromArray);
```

{{ site.data.element.license }}
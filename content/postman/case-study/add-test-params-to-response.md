# Case study: Add test params to API response

```text
URL: {HOST}/api/resource/create
Method: POST
Response: 201 OK
```

### 1

* Na początku endpoint zwracał jedynie kod 201

```text
```

### 2

* Po pierwszej interwencji endpoint zwracał numery z id bazy danych dla stworzonych zasobów

```text
1
```

```text
1, 2, 3
```

### 3

* Po drugiej interwencji endpoint nabrał formę json, zwracał w osobnych obiektach numer z bazy danych i numery zasobów
* Było to przydatne do testów Postman oraz pretestów playwright

```json
[
  {
    "id": 4, 
    "resourceNumber": "111-123456789"
  }
]
```

```json
[
  {
    "id": 5, 
    "resourceNumber": "111-234567891"
  },
  {
    "id": 6, 
    "resourceNumber": "111-345678912"
  }
]
```

### 4

* Kilka miesięcy później, przy planowaniu nowej funkcjonalności, postanowiono skorzystać ze zwracanych danych i dodać nowy klucz w zwracanej odpowiedzi z API.
* Tanie, szybkie, efektowne

```json
[
  {
    "id": 7, 
    "resourceNumber": "111-456789123",
    "serialNumber": null
  },
  {
    "id": 8, 
    "resourceNumber": "111-567891235",
    "serialNumber": "ABC123"
  }
]
```

{{ site.data.element.license }}
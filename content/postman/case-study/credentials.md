# Case study: Simple credential test

## Authorized user

* endpoint

```text
{{HOST}}/api/resources/orders/d46baedf-425f-41c0-b05b-8cb44675ee53
```

* Authorisation

```text
Basic:
User: Tester1
Pass: Pass#1
```

* Response code:

```text
200 - OK
```

* Api response

```json
{
  "orderId": "d46baedf-425f-41c0-b05b-8cb44675ee53",
  "userId": "36b56c38-713a-4cfd-a33f-df65ee893182",
  "currency": "PLN",
  "priceTotal": 19.99,
  "cart": [
    {
      "product": "Cookies",
      "productId": "d6a21108-d2c7-44e7-bf24-091514fa76e2",
      "price": 19.99,
      "discount": 0
    }
  ]
}
```

* Prosty test w imieniu użytkownika Tester1 sprawdzamy, czy może wyświetlić dane swojego zamówienia
* Autoryzacja działa zgodnie z oczekiwaniem

## Unauthorized user

* endpoint

```text
{{HOST}}/api/resources/orders/d46baedf-425f-41c0-b05b-8cb44675ee53
```

* Authorisation

```text
Basic:
User: Tester2
Pass: Pass#2
```

* Response code:

```text
404 - Not Found
```

* Api response

```json
{
  "errorMessage": "Order not found"
}
```

* Sprawdzamy, czy można odpytać api o zamówienie Tester1 posługując się danymi Tester2
* Istotnie jest to, żeby pomimo istniejącego zasobu api zwróciło **404 - Not Found**, a nie np. 401 Unauthorized lub 403 Forbidden

## Other scenarios

| login | password | result |
|-------|----------|--------|
| OK    | OK       | 200    |
| OK    | X        | 404    |
| X     | OK       | 404    |
| X     | X        | 404    |

| orderId | credentials | Result |
|---------|-------------|--------|
| OK      | OK          | 200    |
| OK      | X           | 404    |
| X       | OK          | 404    |
| X       | X           | 404    |

|                               | correct credentials (Tester1) | correct credentials (Tester2) |
|-------------------------------|-------------------------------|-------------------------------|
| orderID (Tester1)             | 200                           | 404                           |

{{ site.data.element.license }}
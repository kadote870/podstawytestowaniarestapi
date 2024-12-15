# Zestawy testów zależnie od kodu HTTP

Scenariusz działania systemu:

1. Wysłanie requestu **POST**
2. Request body trafia na serwer
3. **Serwer sprawdza poprawność danych**
   * nie ma? wysyła błąd
4. Serwer sprawdza ustawienia użytkownika-wybór drukarki
   * nie ma? wysyła błąd
5. Serwer przetwarza request
6. Serwer zwraca odpowiedź

```json
{
   "info": {
      "_postman_id": "d8436d41-1e9c-436d-9f4d-c088bb8291ce",
      "name": "200-400-response-codes-tests",
      "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
      "_exporter_id": "28519490"
   },
   "item": [
      {
         "name": "getAll",
         "event": [
            {
               "listen": "test",
               "script": {
                  "exec": [
                     ""
                  ],
                  "type": "text/javascript",
                  "packages": {}
               }
            }
         ],
         "request": {
            "method": "GET",
            "header": [],
            "url": {
               "raw": "https://api.escuelajs.co/api/v1/products/",
               "protocol": "https",
               "host": [
                  "api",
                  "escuelajs",
                  "co"
               ],
               "path": [
                  "api",
                  "v1",
                  "products",
                  ""
               ]
            }
         },
         "response": []
      },
      {
         "name": "getOne",
         "event": [
            {
               "listen": "test",
               "script": {
                  "exec": [
                     "// Przecwycenie respnse body do zmiennej",
                     "const response = pm.response.json()",
                     "// Przechwycenie response code do zmiennej",
                     "const responseCode = pm.response.code",
                     "",
                     "// instukcja warunkowa, kod wykona sie tylko w wypadku kodu 200",
                     "if (responseCode === 200) {",
                     "    pm.test(\"Status code is 200\", function () {",
                     "        pm.response.to.have.status(200);",
                     "    });",
                     "",
                     "    pm.test(\"Typy danych w odpowiedzi są poprawne\", function () {",
                     "        pm.expect(response.id).to.be.a(\"number\");",
                     "        pm.expect(response.title).to.be.a(\"string\");",
                     "        pm.expect(response.price).to.be.a(\"number\");",
                     "        pm.expect(response.description).to.be.a(\"string\");",
                     "        pm.expect(response.images).to.be.an(\"array\");",
                     "        pm.expect(response.creationAt).to.be.a(\"string\");",
                     "        pm.expect(response.updatedAt).to.be.a(\"string\");",
                     "        pm.expect(response.category).to.be.a(\"object\");",
                     "        pm.expect(response.category.id).to.be.a(\"number\");",
                     "        pm.expect(response.category.name).to.be.a(\"string\");",
                     "        pm.expect(response.category.image).to.be.a(\"string\");",
                     "        pm.expect(response.category.creationAt).to.be.a(\"string\");",
                     "        pm.expect(response.category.updatedAt).to.be.a(\"string\");",
                     "    });",
                     "    // jeśli nie ma kodu 200 nastepny do sprawdzenia jest kod 400",
                     "} else if (responseCode === 400) {",
                     "    pm.test(\"Status code is 400\", function () {",
                     "        pm.response.to.have.status(400);",
                     "    });",
                     "",
                     "    pm.test('Endpoint display correct message - \"EntityNotFoundError\"', function () {",
                     "        pm.expect(response.name).to.eql(\"EntityNotFoundError\");",
                     "    });",
                     "    // jeśli nie było kodu 200 lub 400 to zostanie wykonany poniższy kod",
                     "} else {",
                     "    pm.test(`Api send code ${responseCode},  test scenario allow only to code 200 or 400`, function () {",
                     "        pm.response.to.have.status(600);",
                     "    });",
                     "}",
                     "",
                     ""
                  ],
                  "type": "text/javascript",
                  "packages": {}
               }
            }
         ],
         "request": {
            "method": "GET",
            "header": [],
            "url": {
               "raw": "https://api.escuelajs.co/api/v1/products/47",
               "protocol": "https",
               "host": [
                  "api",
                  "escuelajs",
                  "co"
               ],
               "path": [
                  "api",
                  "v1",
                  "products",
                  "47"
               ]
            }
         },
         "response": []
      }
   ]
}
```
# Wysyłanie prerequest

```json
{
	"info": {
		"_postman_id": "c9fbb8f7-0f40-4491-a3d2-3a78d46d5664",
		"name": "prerequest",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "28519490"
	},
	"item": [
		{
			"name": "getOne",
			"event": [
				{
					"listen": "test",
					"script": {
						"exec": [
							"const response = pm.response.json()",
							"",
							"pm.test(\"Status code is 200\", function () {",
							"    pm.response.to.have.status(200);",
							"});",
							"",
							"pm.test(\"Typy danych w odpowiedzi są poprawne\", function () {",
							"    pm.expect(response.id).to.be.a(\"number\");",
							"    pm.expect(response.title).to.be.a(\"string\");",
							"    pm.expect(response.price).to.be.a(\"number\");",
							"    pm.expect(response.description).to.be.a(\"string\");",
							"    pm.expect(response.images).to.be.an(\"array\");",
							"    pm.expect(response.creationAt).to.be.a(\"string\");",
							"    pm.expect(response.updatedAt).to.be.a(\"string\");",
							"    pm.expect(response.category).to.be.a(\"object\");",
							"    pm.expect(response.category.id).to.be.a(\"number\");",
							"    pm.expect(response.category.name).to.be.a(\"string\");",
							"    pm.expect(response.category.image).to.be.a(\"string\");",
							"    pm.expect(response.category.creationAt).to.be.a(\"string\");",
							"    pm.expect(response.category.updatedAt).to.be.a(\"string\");",
							"});",
							""
						],
						"type": "text/javascript",
						"packages": {}
					}
				},
				{
					"listen": "prerequest",
					"script": {
						"exec": [
							"// Podstawa kodu z snippeta - \"Send a request\" - ten kod bedzie wysylac request do api",
							"try {",
							"    // Kod wysyła request do api i przechoduje go w zmiennej",
							"    const request = await pm.sendRequest({",
							"        url: \"https://api.escuelajs.co/api/v1/products/\",",
							"        method: \"GET\"",
							"    });",
							"",
							"    // Przetworzenie do takiego formatu żeby można było pracować na odpowiedzi z API",
							"    const response = request.json()",
							"",
							"    // Pusta teblica",
							"    const productIds = []",
							"    // Petla, która wpycha do tablicy dane - ID z każdego napotkanego obiektu",
							"    for (const element of response) {",
							"        productIds.push(element.id)",
							"    }",
							"",
							"    // Losowanie z tablicy jednej zmiennej",
							"    function get_random_value_from_array(arr) {",
							"        return arr[Math.floor(Math.random() * arr.length)];",
							"    }",
							"    const randomValueFromArray = get_random_value_from_array(productIds);",
							"",
							"    // Umieszczenie losowej zmiennej jako \"zmienną globalną\" postman",
							"    pm.globals.set('randomProductId',randomValueFromArray)",
							"} catch (err) {",
							"    console.error(err);",
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
					"raw": "https://api.escuelajs.co/api/v1/products/{{randomProductId}}",
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
						"{{randomProductId}}"
					]
				}
			},
			"response": []
		}
	]
}
```
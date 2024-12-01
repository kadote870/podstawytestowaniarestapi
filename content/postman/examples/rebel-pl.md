# Rebel-pl direct products urls creator

## Postman
```json
{
  "info": {
    "_postman_id": "b1550192-80bf-4bf0-ba4f-2bb46e9656bd",
    "name": "rebel.pl",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
    "_exporter_id": "28519490"
  },
  "item": [
    {
      "name": "shopping",
      "item": [
        {
          "name": "cart",
          "item": [
            {
              "name": "info",
              "request": {
                "method": "GET",
                "header": [],
                "url": {
                  "raw": "https://www.rebel.pl/shopping/cart/info",
                  "protocol": "https",
                  "host": [
                    "www",
                    "rebel",
                    "pl"
                  ],
                  "path": [
                    "shopping",
                    "cart",
                    "info"
                  ]
                }
              },
              "response": []
            },
            {
              "name": "edit",
              "event": [
                {
                  "listen": "prerequest",
                  "script": {
                    "exec": [
                      "const cookie = 'cookie value'",
                      "",
                      "pm.globals.set('cookie',cookie)"
                    ],
                    "type": "text/javascript",
                    "packages": {}
                  }
                }
              ],
              "protocolProfileBehavior": {
                "disabledSystemHeaders": {
                  "connection": true,
                  "accept-encoding": true,
                  "accept": true,
                  "content-length": true,
                  "user-agent": true
                }
              },
              "request": {
                "method": "PUT",
                "header": [
                  {
                    "key": "Cookie",
                    "value": "{{cookie}}"
                  }
                ],
                "url": {
                  "raw": "https://www.rebel.pl/shopping/cart/edit/{{productId}}/1",
                  "protocol": "https",
                  "host": [
                    "www",
                    "rebel",
                    "pl"
                  ],
                  "path": [
                    "shopping",
                    "cart",
                    "edit",
                    "{{productId}}",
                    "1"
                  ]
                },
                "description": "Generated from cURL: curl 'https://www.rebel.pl/shopping/cart/edit/9665/2' \\\n  -X 'PUT' \\\n  -H 'Accept: */*' \\\n  -H 'Accept-Language: pl-PL,pl;q=0.6' \\\n  -H 'Connection: keep-alive' \\\n  -H 'Content-Length: 0' \\\n  -H 'Cookie: Sklep2Session=mm3gtk8jf9fnqebf3oc1ioidig; one_zl_promo=2002325|2008015' \\\n  -H 'Origin: https://www.rebel.pl' \\\n  -H 'Referer: https://www.rebel.pl/shopping/cart' \\\n  -H 'Sec-Fetch-Dest: empty' \\\n  -H 'Sec-Fetch-Mode: cors' \\\n  -H 'Sec-Fetch-Site: same-origin' \\\n  -H 'Sec-GPC: 1' \\\n  -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36' \\\n  -H 'X-Requested-With: XMLHttpRequest' \\\n  -H 'dnt: 1' \\\n  -H 'sec-ch-ua: \"Brave\";v=\"131\", \"Chromium\";v=\"131\", \"Not_A Brand\";v=\"24\"' \\\n  -H 'sec-ch-ua-mobile: ?0' \\\n  -H 'sec-ch-ua-platform: \"macOS\"'"
              },
              "response": []
            }
          ]
        }
      ]
    },
    {
      "name": "api",
      "item": [
        {
          "name": "products",
          "item": [
            {
              "name": "latest",
              "item": [
                {
                  "name": "100",
                  "event": [
                    {
                      "listen": "test",
                      "script": {
                        "exec": [
                          "const response = pm.response.json()",
                          "const preorders = response.content",
                          "const urls = []",
                          "",
                          "for (const element of preorders) {",
                          "    const url = 'https://www.rebel.pl/gry-planszowe/postman-' + element.objectID + '.html'",
                          "    urls.push(url)",
                          "}",
                          "",
                          "console.log(urls)",
                          "",
                          "function get_random_value_from_array(arr) {",
                          "    return arr[Math.floor(Math.random() * arr.length)];",
                          "}",
                          "const randomValueFromArray = get_random_value_from_array(response.content);",
                          "const productId = randomValueFromArray.objectID",
                          "pm.globals.set('productId', productId)"
                        ],
                        "type": "text/javascript",
                        "packages": {}
                      }
                    }
                  ],
                  "request": {
                    "method": "GET",
                    "header": [
                      {
                        "key": "X-Requested-With",
                        "value": "XMLHttpRequest",
                        "type": "text"
                      }
                    ],
                    "url": {
                      "raw": "https://www.rebel.pl/api/products/latest/100",
                      "protocol": "https",
                      "host": [
                        "www",
                        "rebel",
                        "pl"
                      ],
                      "path": [
                        "api",
                        "products",
                        "latest",
                        "100"
                      ]
                    },
                    "description": "Generated from cURL: curl 'https://www.rebel.pl/api/products/preorders' \\\n  -H 'Accept: */*' \\\n  -H 'Accept-Language: pl-PL,pl;q=0.8' \\\n  -H 'Connection: keep-alive' \\\n  -H 'Cookie: Sklep2Session=l1ogcknbl6jmvabmi014mtnmga' \\\n  -H 'Referer: https://www.rebel.pl/' \\\n  -H 'Sec-Fetch-Dest: empty' \\\n  -H 'Sec-Fetch-Mode: cors' \\\n  -H 'Sec-Fetch-Site: same-origin' \\\n  -H 'Sec-GPC: 1' \\\n  -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36' \\\n  -H 'X-Requested-With: XMLHttpRequest' \\\n  -H 'sec-ch-ua: \"Brave\";v=\"131\", \"Chromium\";v=\"131\", \"Not_A Brand\";v=\"24\"' \\\n  -H 'sec-ch-ua-mobile: ?0' \\\n  -H 'sec-ch-ua-platform: \"macOS\"'"
                  },
                  "response": []
                }
              ]
            },
            {
              "name": "preorders",
              "event": [
                {
                  "listen": "test",
                  "script": {
                    "exec": [
                      "const response = pm.response.json()",
                      "const preorders = response.content",
                      "const urls = []",
                      "",
                      "for (const element of preorders) {",
                      "    const url = 'https://www.rebel.pl/gry-planszowe/postman-' + element.objectID + '.html'",
                      "    urls.push(url)",
                      "}",
                      "",
                      "console.log(urls)",
                      "",
                      "function get_random_value_from_array(arr) {",
                      "    return arr[Math.floor(Math.random() * arr.length)];",
                      "}",
                      "const randomValueFromArray = get_random_value_from_array(response.content);",
                      "const productId = randomValueFromArray.objectID",
                      "pm.globals.set('productId', productId)"
                    ],
                    "type": "text/javascript",
                    "packages": {}
                  }
                }
              ],
              "request": {
                "method": "GET",
                "header": [
                  {
                    "key": "X-Requested-With",
                    "value": "XMLHttpRequest",
                    "type": "text"
                  }
                ],
                "url": {
                  "raw": "https://www.rebel.pl/api/products/preorders",
                  "protocol": "https",
                  "host": [
                    "www",
                    "rebel",
                    "pl"
                  ],
                  "path": [
                    "api",
                    "products",
                    "preorders"
                  ]
                },
                "description": "Generated from cURL: curl 'https://www.rebel.pl/api/products/preorders' \\\n  -H 'Accept: */*' \\\n  -H 'Accept-Language: pl-PL,pl;q=0.8' \\\n  -H 'Connection: keep-alive' \\\n  -H 'Cookie: Sklep2Session=l1ogcknbl6jmvabmi014mtnmga' \\\n  -H 'Referer: https://www.rebel.pl/' \\\n  -H 'Sec-Fetch-Dest: empty' \\\n  -H 'Sec-Fetch-Mode: cors' \\\n  -H 'Sec-Fetch-Site: same-origin' \\\n  -H 'Sec-GPC: 1' \\\n  -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36' \\\n  -H 'X-Requested-With: XMLHttpRequest' \\\n  -H 'sec-ch-ua: \"Brave\";v=\"131\", \"Chromium\";v=\"131\", \"Not_A Brand\";v=\"24\"' \\\n  -H 'sec-ch-ua-mobile: ?0' \\\n  -H 'sec-ch-ua-platform: \"macOS\"'"
              },
              "response": []
            }
          ]
        },
        {
          "name": "index",
          "item": [
            {
              "name": "bestsellers",
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
                },
                {
                  "listen": "prerequest",
                  "script": {
                    "packages": {},
                    "type": "text/javascript"
                  }
                }
              ],
              "protocolProfileBehavior": {
                "disabledSystemHeaders": {
                  "connection": true,
                  "accept": true,
                  "accept-encoding": true,
                  "user-agent": true
                }
              },
              "request": {
                "method": "GET",
                "header": [
                  {
                    "key": "X-Requested-With",
                    "value": "XMLHttpRequest",
                    "type": "text"
                  }
                ],
                "url": {
                  "raw": "https://www.rebel.pl/api/index/bestsellers",
                  "protocol": "https",
                  "host": [
                    "www",
                    "rebel",
                    "pl"
                  ],
                  "path": [
                    "api",
                    "index",
                    "bestsellers"
                  ]
                },
                "description": "Generated from cURL: curl 'https://www.rebel.pl/api/products/preorders' \\\n  -H 'Accept: */*' \\\n  -H 'Accept-Language: pl-PL,pl;q=0.8' \\\n  -H 'Connection: keep-alive' \\\n  -H 'Cookie: Sklep2Session=l1ogcknbl6jmvabmi014mtnmga' \\\n  -H 'Referer: https://www.rebel.pl/' \\\n  -H 'Sec-Fetch-Dest: empty' \\\n  -H 'Sec-Fetch-Mode: cors' \\\n  -H 'Sec-Fetch-Site: same-origin' \\\n  -H 'Sec-GPC: 1' \\\n  -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36' \\\n  -H 'X-Requested-With: XMLHttpRequest' \\\n  -H 'sec-ch-ua: \"Brave\";v=\"131\", \"Chromium\";v=\"131\", \"Not_A Brand\";v=\"24\"' \\\n  -H 'sec-ch-ua-mobile: ?0' \\\n  -H 'sec-ch-ua-platform: \"macOS\"'"
              },
              "response": []
            }
          ]
        }
      ]
    }
  ]
}
```

## HTML (gpt)

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wyświetlanie adresów URL</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            background-color: #f9f9f9;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            margin: 10px 0;
        }
        a {
            text-decoration: none;
            color: #007BFF;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <h1>Lista adresów URL</h1>
    <ul id="urlList"></ul>

    <script>
        // Tablica URL
        const url = [   'https://www.example.com/path-to-content-01.html',
  'https://www.example.com/path-to-content-02.html',
  'https://www.example.com/path-to-content-03.html',
  'https://www.example.com/path-to-content-04.html',
  'https://www.example.com/path-to-content-05.html',
  'https://www.example.com/path-to-content-06.html' ];

        // Pobranie elementu listy z HTML
        const urlList = document.getElementById("urlList");

        // Generowanie listy linków
        url.forEach((address) => {
            const listItem = document.createElement("li");
            const link = document.createElement("a");
            link.href = address;
            link.textContent = address;
            link.target = "_blank"; // Otwiera link w nowej karcie
            listItem.appendChild(link);
            urlList.appendChild(listItem);
        });
    </script>
</body>
</html>

```
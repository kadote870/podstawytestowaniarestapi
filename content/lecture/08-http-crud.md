# 08 - Podstawowe metody żądań HTTP a CRUD

<a href="https://miroslawmamczur.pl/czym-jest-api-i-jakie-sa-jego-rodzaje/">
    <img src="https://codestoresolutions.com/wp-content/uploads/2023/08/crud.webp" height="250">
</a>

| CRUD   | HTTTP                                      | SQL    | REST                      |
|--------|--------------------------------------------|--------|---------------------------|
| Create | <span style="color:orange">**POST**</span> | INSERT | ```{host}/api/movie```    |
| Read   | <span style="color:green">**GET**</span>   | SELECT | ```{host}/api/movie/id``` |
| Update | <span style="color:blue">**PUT**</span>    | UPDATE | ```{host}/api/movie```    |
| Delete | <span style="color:red">**DELETE**</span>  | DELETE | ```{host}/api/movie/id``` |

<span style="color:green">**GET**</span>: Metoda GET służy do pobrania reprezentacji określonego zasobu. Żądania GET
powinny służyć tylko do odbierania danych.
<br><br>
<span style="color:orange">**POST**</span>: Metoda POST służy do przesłania danych do określonego zasobu, często
powodując zmianę stanu lub skutkując efektami ubocznymi po stronie serwera, często
dodaje nowy zasób.
<br><br>
<span style="color:blue">**PUT**</span>: Metoda PUT służy do zastąpienia wszystkich obecnych reprezentacji docelowego
zasobu danymi przesłanymi w żądaniu.
<br><br>
<span style="color:red">**DELETE**</span>: Metoda DELETE służy do usuwania określonego zasobu.

## REST API daje dodatkową możliwość dla operacji update - PATCH

| CRUD   | HTTTP                                      | SQL    | REST                      |
|--------|--------------------------------------------|--------|---------------------------|
| Create | <span style="color:orange">**POST**</span> | INSERT | ```{host}/api/movie```    |
| Read   | <span style="color:green">**GET**</span>   | SELECT | ```{host}/api/movie/id``` |
| Update | <span style="color:blue">**PUT**</span>    | UPDATE | ```{host}/api/movie```    |
| Update | **PATCH**                                  | UPDATE | ```{host}/api/movie```    |
| Delete | <span style="color:red">**DELETE**</span>  | DELETE | ```{host}/api/movie/id``` |

<span style="color:blue">**PUT**</span>: Metoda <span style="color:blue">**PUT**</span> służy do
zastąpienia <span style="color:red">**wszystkich obecnych**</span> reprezentacji docelowego
zasobu danymi przesłanymi w żądaniu.

**PATCH**: Metoda **PATCH** służy do zastąpienia <span style="color:red">**wybranych parametrów**</span> wybranego
zasobu.

<a href="https://javacodehouse.com/blog/REST-put-vs-patch/">
    <img src="https://javacodehouse.com/assets/img/thumb/PUT-vs-PATCH.svg" height="250">
</a>

### Następny rozdział: [09 - Typy uwierzytelniania w protokole HTTP](09-typy-uwierzytelniania.md)
# Cache w REST API

> 💡 W procesie testowania REST API (operacje CRUD, asercje itd. nie ma to większego znaczenia) ⚙️

## HTTP REQUEST (Żądanie HTTP)

<a href="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/HTTP_Basics.html">
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_RequestMessageExample.png">
</a>

## HTTP RESPONSE (Odpowiedź HTTP)

<a href="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/HTTP_Basics.html">
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_ResponseMessageExample.png">
</a>

## Przykład:

```text
HTTP/1.1 200 OK
Cache-Control: max-age=3600, public
ETag: "xyz123"
Content-Type: application/json
```

1. Klient wysyła pierwsze żądanie
2. Kolejne zapytanie klienta (np. po 30 minutach) ⏳
3. Przeglądarka sprawdza, czy odpowiedź jest w cache (max-age=3600, czyli 1h)
4. API wysyła na serwer zapytanie z nagłówkiem  ```ETag: "xyz123"```
5. Serwer sprawdza, czy dane się zmieniły

💡 WARIANT 1: DANE SIĘ **NIE** ZMIENIŁY:

* Serwer odpowiada ```304 Not Modified``` (bez treści, oszczędność transferu) 💾
* Przeglądarka korzysta z lokalnej kopii danych 🖥️

<br>

💡 WARIANT 2: DANE SIĘ ZMIENIŁY:

* Przeglądarka wykonuje nowe zapytanie i pobiera dane 🔄

### ⏭️ Powrót do: [07 - REST API 🌐](../07-rest-api.md)
# Task 04 - HTTP Authorization request header

* Utwórz kolekcję **Task 04**
* Utwórz zapytanie GET, dla którego zwrócony będzie status 200 (OK):

<br>

* **Autoryzacja Basic Auth**
    * ```https://httpbin.org/basic-auth/user/pass```
    * Username: ```user```
    * Password: ```pass```
* [Base64 DEcode](https://www.base64decode.org/) [Base64 ENcode](https://www.base64encode.org/)

> * 🔐 Base64 to kodowanie, **NIE** szyfrowanie! ❌🔒
> * Umożliwia łatwe przesyłanie danych, ale nie chroni ich przed ciekawskimi oczami 👀
> * To sposób na przedstawienie danych binarnych w formie tekstowej! 💻📤

<br>

* **Autoryzacja Bearer Auth**
    * ```https://httpbin.org/bearer```
    * Token: ```07032023```

> * 💡 Token Bearer nie jest szyfrowany – to ciąg znaków do uwierzytelniania, często w formacie JWT (JSON Web Token),
    kodowany w Base64url, ale czytelny po dekodowaniu. 🔑
> * 💡 Nie umieszczaj w nim wrażliwych danych. JWS (JSON Web Signature) jest podpisany, ale nie ukrywa treści, JWE (JSON
    Web Encryption) jest szyfrowane, ale rzadziej używane. Opaque tokeny (losowe ciągi znaków) wymagają weryfikacji na
    serwerze. 🔒
> * 💡 Token nie jest szyfrowany, więc dbaj o jego bezpieczeństwo. ⚠️

<br>

* **Autoryzacja Digest Auth**
    * ```https://httpbin.org/digest-auth/auth/user/pass```
    * Username: ```user```
    * Password: ```pass```

> * 🧑‍💻 Klient wysyła zapytanie do serwera.
> * 💬 Serwer odpowiada z unikalnym identyfikatorem i dodatkowymi danymi.
> * 🔐 Klient generuje hasz z tych informacji i wysyła go w nagłówku "Authorization".
> * ✅ Serwer weryfikuje hasz, porównując go z oczekiwanym haszem, który oblicza na podstawie zapisanych danych
    użytkownika.

<br>

* Zabezpiecz loginy i hasła przed ewentualnym wyciekiem

### Następny rozdział: [Task 05 - Trello](05-task-trello.md)

# 04 - HTTP - Warstwa 7 modelu OSI

* Hypertext Transfer Protocol (HTTP)
* Jest protokołem używanym do komunikacji między serwerami internetowymi a klientami (takimi jak przeglądarki
  internetowe) w internecie.
* Stworzony przez [Tima Bernersa-Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee)
* HTTP jest protokołem żądanie-odpowiedź, gdzie klient wysyła żądanie do serwera dotyczące określonego
  zasobu (takiego jak strona internetowa), a serwer
  odpowiada żądanym zasobem.
* HTTP jest protokołem **bezstanowym**, co oznacza, że **każde żądanie jest niezależne** i nie polega na żadnych
  wcześniejszych żądaniach.
* HTTP korzysta z zestawu metod (takich jak <span style="color:darkred"> **GET, POST,
  PUT, DELETE** </span>), aby wskazać rodzaj żądania składanego
  przez klienta.

> 💡 W rzeczywistości istnieje więcej metod HTTP Request: GET, HEAD, POST, PUT, DELETE, TRACE, OPTIONS, CONNECT

* HTTP wykorzystuje również kody statusu (takie jak 200
  OK, 404 Not Found, 500 Internal Server Error), aby
  wskazać sukces lub niepowodzenie żądania.

## CECHY PROTOKOŁU HTTP

**Prostota**: HTTP jest prostym i lekkim protokołem, który jest łatwy do zrozumienia i używania. Jest oparty na
tekście, co ułatwia odczytywanie i debugowanie.
<br>

**Kompatybilność**: HTTP jest kompatybilny z szerokim spektrum technologii i platform, co
czyni go idealnym wyborem do budowy aplikacji internetowych.
<br>

**Elastyczność**: HTTP to elastyczny protokół, który umożliwia przesyłanie różnych rodzajów
danych przez internet, w tym tekstów, obrazów, dźwięku i wideo.
<br>

**Caching**: HTTP obsługuje mechanizm cachowania, który umożliwia przechowywanie często
odwiedzanych zasobów lokalnie po stronie klienta, poprawiając wydajność i redukując
obciążenie serwera.<br>

**Bezstanowość**: HTTP jest protokołem bezstanowym, co oznacza, że każde żądanie klienta
do serwera jest niezależne i nie polega na wcześniejszych żądaniach. Ułatwia to skalowanie
aplikacji internetowych i obsługę dużego ruchu.

## HTTP REQUEST (Żądanie HTTP)

<a href="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/HTTP_Basics.html">
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_RequestMessageExample.png">
</a>

## HTTP RESPONSE (Odpowiedź HTTP)

<a href="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/HTTP_Basics.html">
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_ResponseMessageExample.png">
</a>

## HTTP HEADERS (Nagłówki HTTP)

* **Authorization** – Najczęściej zawiera wartość, która służy autoryzacji i uwierzytelnieniu użytkownika, na przykład
  token, apiKey, nazwę użytkownika i hasło, etc.
* **Cookie** – Służy do zwracania wartości ciasteczek przesłanych wcześniej z wykorzystaniem Set-Cookie.
* **Set-Cookie** – Pozwala na wysłanie zawartości ciasteczka do serwera.
* **User-Agent** – Definiuje jaki program/aplikacja wykonała zapytanie. Należy pamiętać, że tak jak inne wartości
  nagłówków HTTP, User-Agent również może zawierać dowolną wartość zdefiniowaną przez klienta.

<br>

* **Cache-Control** – Zawiera wytyczne dla mechanizmów cache.
* **Expires** – Definiuje, jak długo zwrócona przez serwer odpowiedź może być uznana za aktualną.
* **ETag** – Określa identyfikator określonej wersji zasobu. Gdy zasób po stronie serwera zostanie zmodyfikowany, jego
  ETag również powinien ulec zmianie.
* **Connection** – Pozwala zdefiniować, czy połączenie po dokonaniu transakcji zostanie zerwane czy też nie. Z
  wykorzystaniem tego nagłówka należy być ostrożnym. Nierozważne wykorzystywanie wartości keep-alive, czyli podtrzymania
  połączenia, może doprowadzić do powstania dużej puli niezamkniętych połączeń co jest potencjalnym polem do powstania
  problemów wydajnościowych w aplikacji.
* **Accept** – Wskazuje format zawartości (MIME type), jakiego klient się spodziewa.
* **Content-Type** – Analogiczny nagłówek do Accept, z tym że zwracany jest w odpowiedzi. Content-Type definiuje, w
  jakim formacie została zwrócona odpowiedź.
* **Accept-Language** – Definiuje spodziewany przez klienta język odpowiedzi.
* **Content-Length** – Zawiera wartość określającą długość body w odpowiedzi zapytania.
* **Content-Encoding** – Definiuje rodzaj zastosowanej kompresji odpowiedzi.
* **Location** – Zwraca lokalizację do zasobu. Wykorzystywany jest w przypadku przekierowań lub po utworzeniu nowego
  zasobu na serwerze.
* **Referer** – Zawiera źródło (URL) pochodzenia zapytania. Zwróć uwagę, że nagłówek nazywa się **Referer**, a nie 
**Referrer**! Jest to dość niefortunna **literówka**, która weszła do standardu HTTP.
* **Origin** – Zawiera domenę pochodzenia zapytania. Wykorzystywane najczęściej przy mechanizmach CORS (Cross Origin
  Resource Sharing).

## HTTP RESPONSE CODES (Kody odpowiedzi HTTP)

1xx: Informational (żądanie zostało otrzymane i jest przetwarzane):

> * **100** Continue: Serwer otrzymał nagłówki żądania i klient powinien kontynuować wysyłanie ciała żądania.


**<span style="color:green">2xx: Success</span> (żądanie zostało pomyślnie otrzymane, zrozumiane i zaakceptowane):**

> * **200** OK: Serwer pomyślnie przetworzył żądanie.
> * **204** No Content: Serwer pomyślnie przetworzył żądanie, ale nie ma ciała odpowiedzi do zwrócenia.

<span style="color:orange">3xx: Redirection</span> (wymagane jest podjęcie dalszych działań w celu ukończenia żądania)
> * **301** Moved Permanently: Żądany zasób został trwale przeniesiony na nowe miejsce.
> * **302** Found: Żądany zasób został tymczasowo przeniesiony na nowe miejsce, przyszłe żądania powinny używać nowego
    adresu URL.

**<span style="color:red">4xx: Client Error</span> (żądanie zawiera błędną składnię lub nie można go zrealizować):**
> * **400** Bad Request: Żądanie nie mogło zostać zrozumiane lub brakowało wymaganych parametrów.
> * **404** Not Found: Żądany zasób nie został odnaleziony na serwerze.
> * uwaga na kod **418** 🫖

**<span style="color:blue">5xx: Server Error</span> (serwer nie był w stanie spełnić pozornie poprawnego żądania)**
> * **500** Internal Server Error: Serwer napotkał nieoczekiwany błąd uniemożliwiający realizację żądania.
> * **503** Service Unavailable: Serwer jest obecnie niezdolny do obsłużenia żądania z powodu tymczasowego przeciążenia
    lub konserwacji.

LINKI:

* [Kody HTTP — w3schools.com](https://www.w3schools.com/tags/ref_httpmessages.asp)
* [Kody HTTP — developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
* [Kotki HTTP — http.cat](https://http.cat/) 🐱
* [Pieski HTTP — http.dog](https://http.dog/) 🐶

### ⏭️ Następny rozdział: [05 - Od prostych do złożonych usług internetowych](05-od-prostych-do-zlozonych-uslug-internetowych.md)

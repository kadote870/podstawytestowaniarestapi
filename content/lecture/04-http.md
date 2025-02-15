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
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_RequestMessageExample.png" width="534">
</a>


## HTTP RESPONSE (Odpowiedź HTTP)
<a href="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/HTTP_Basics.html">
    <img src="https://personal.ntu.edu.sg/ehchua/programming/webprogramming/images/HTTP_ResponseMessageExample.png" width="534">
</a>


# Następny rozdział: [05 - Od prostych do złożonych usług internetowych](05-od-prostych-do-zlozonych-uslug-internetowych.md)

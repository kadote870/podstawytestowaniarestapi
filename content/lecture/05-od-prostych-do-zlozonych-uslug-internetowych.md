# 05 - Od prostych do złożonych usług internetowych

<a href="https://en.wikipedia.org/wiki/Client%E2%80%93server_model">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Client-server-model.svg">
</a>

* HTML pozwala na tworzenie stron internetowych
* Na początku istnienia współczesnego Internetu, rozwiązanie to polegało na wysłaniu całego pliku (fragmentu) strony
  internetowej
* Wysyłano żądanie do serwera, a serwer wysyłał dane
* Do komunikacji pomiędzy klientem a serwerem służy HTTP
* Z czasem strony internetowe zaczęły być coraz bardziej złożone i skomplikowane (dużo danych)
* Dawniej przepustowość Internetu była tysiące razy niższa niż na współczesnych światłowodach.
* Następnym krokiem w ewolucji Internetu było opracowywanie rozwiązań, których celem było „odchudzenie” transferu
  potrzebnego do korzystania z konkretnej strony internetowej

<br>

* Przykład: [gofundme](https://www.gofundme.com/f/neseblod-records-fire-fund?modal=donations&tab=all)
    * serwer wysyła nam tylko takie informacje, jakie nam są potrzebne
    * youtube, instagram, spotify
    * pomiędzy klientem a serwerem istnieje pewien pomost komunikacyjny
    * jest to właśnie API
    * dane są podsyłane fragmentami, są dawkowane

# Następny rozdział: [06 - API](06-api.md)
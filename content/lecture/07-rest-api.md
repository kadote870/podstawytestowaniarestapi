# 07 - REST API 🌐

* REST API to nie jest osobna technologia, tylko zbiór zasad projektowania API
* Bazuje na HTTP

### REST (Representational State Transfer)

1. **Representational (Reprezentacyjny)**
    * Dane (zasoby) są przesyłane między klientem a serwerem w różnych reprezentacjach (np. JSON, XML, HTML).
    * Klient żąda zasobu, a serwer zwraca jego reprezentację.
2. **State (Stan)**
    * Każda operacja na zasobie może zmieniać jego stan (np. zmiana danych w bazie).
    * REST jest bezstanowy, co oznacza, że każdy request od klienta musi zawierać wszystkie informacje potrzebne do
      jego obsługi – serwer nie przechowuje informacji o wcześniejszych żądaniach.
3. **Transfer (Transfer)**
    * Dane są przesyłane między klientem a serwerem za pomocą standardowych metod HTTP (GET, POST, PUT, PATCH, DELETE
      itd.).

## 6 Zasad projektowania REST API

### #1

* Interfejs powinien zapewniać ustandaryzowaną komunikację między klientem a serwerem
* Projektujemy jeden interfejs odpowiadamy na potrzeby wszystkich aplikacji

### #2

* Wyraźny podział między klientem a aplikacją po stronie klienta (front) i serwera (backend)
* Dzięki temu mogą się niezależnie od siebie rozwijać i zmieniać

### #3

* Każde zapytanie musi posiadać komplet informacji koniecznych do jego poprawnego
  zakończenia.

> 💡 Np. Za każdym razem musimy wysłać dane autoryzacyjne 🔑

* Serwer nie przechowuje informacji o stanie klienta (front).
* Klient nie przechowuje informacji o stanie serwera (backend).

> 💡 Np. możemy wielokrotnie wysyłać request o usunięcie tego samego zasobu 🔄

* W zamian klient za każdym razem dostarcza informacje, które umożliwią serwerowi określenie czy dany klient ma
  dostęp do danych zasobów, czy nie.

### #4

W celu zwiększenia wydajności REST API jest cache'owalne.
> 💡 W procesie testowania REST API (operacje CRUD, asercje itd. nie ma to większego znaczenia) ⚙️

```text
HTTP/1.1 200 OK
Cache-Control: max-age=3600, public
ETag: "xyz123"
Content-Type: application/json
```

> 1. Klient wysyła pierwsze żądanie
> 2. Kolejne zapytanie klienta (np. po 30 minutach) ⏳
> 3. Przeglądarka sprawdza, czy odpowiedź jest w cache (max-age=3600, czyli 1h)
> 4. API wysyła na serwer zapytanie z nagłówkiem  ```ETag: "xyz123"```
> 5. Serwer sprawdza, czy dane się zmieniły
>
> 💡 WARIANT 1: DANE SIĘ **NIE** ZMIENIŁY:
> * Serwer odpowiada ```304 Not Modified``` (bez treści, oszczędność transferu) 💾
> * Przeglądarka korzysta z lokalnej kopii danych 🖥️
>
> 💡 WARIANT 2: DANE SIĘ ZMIENIŁY:
> * Przeglądarka wykonuje nowe zapytanie i pobiera dane 🔄

### #5

Projektowanie API i systemu powinno uwzględniać to, żeby klient nie wiedział, co się dzieje po
stronie serwera. I może być tak, że serwer, zanim przygotuje odpowiedź, może wykonać kilka
dodatkowych akcji.
> * 💡 Ochrona danych i infrastruktury organizacji 🛡️
> * 💡 Odciążenie urządzenia klienta 🖱️

### #6 (opcjonalna)

* Code on demand
* To możliwość przesłania fragmentu kodu, który będzie wykonany po stronie klienta/serwera

## Warto zobaczyć
* ➡️ Film: [Stop Calling Your API a "REST API"](https://www.youtube.com/watch?v=0vC4Xt4wqTk)

### Następny rozdział: [08 - Podstawowe metody żądań HTTP a CRUD](08-http-crud.md)
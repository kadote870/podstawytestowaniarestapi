# 07 - REST API 🌐

* 👉 REST API to nie jest osobna technologia, tylko zbór zasad projektowania API
* 👉 Bazuje na protokole HTTP ⚡

### REST (Representational State Transfer)

1. **Representational (Reprezentacyjny)**
    * 📦 Dane (zasoby) są przesyłane między klientem a serwerem w różnych reprezentacjach (np. JSON, XML, HTML)
    * 📤 Klient żąda zasobu, a serwer zwraca jego reprezentację
2. **State (Stan)**
    * 🔄 Każda operacja na zasobie może zmieniać jego stan (np. zmiana danych w bazie)
    * ❌ REST jest bezstanowy, co oznacza, że każdy request od klienta musi zawierać wszystkie informacje potrzebne do
      jego obsługi – serwer nie przechowuje informacji o wcześniejszych żądaniach
3. **Transfer (Transfer)**
    * 📡 Dane są przesyłane między klientem a serwerem za pomocą standardowych metod HTTP (<span style="color:green">**GET**</span>, <span style="color:orange">**POST**</span>, <span style="color:blue">**PUT**</span>, **PATCH**, <span style="color:red">**DELETE**</span>itd.)

## 🏠 6 Zasad projektowania REST API

### #1 🔄 **Spójny interfejs**

* Interfejs powinien zapewniać **ustandaryzowaną komunikację** między klientem a serwerem
* Projektujemy **jeden interfejs**, który odpowiada na potrzeby różnych aplikacji

### #2 ✂️ **Podział na klienta i serwer**

* Wyraźny podział między klientem (frontend) i serwerem (backend)
* Dzięki temu mogą **rozwijać się niezależnie** i nie wpływać na siebie nawzajem

### #3 🔑 **Bezstanowość**

* Każde zapytanie musi zawierać **komplet informacji** wymaganych do jego obsługi

> 💡 **Przykład**: Za każdym razem musimy wysłać dane autoryzacyjne 🔑

* Serwer **nie przechowuje informacji** ❌ o stanie klienta (frontend)
* Klient **nie przechowuje informacji** ❌ o stanie serwera (backend)

> 💡 **Przykład**: Możemy wielokrotnie wysyłać request o usunięcie tego samego zasobu 🔄

✔️ Klient zawsze **przekazuje wszystkie niezbędne informacje**, aby serwer mógł określić, czy użytkownik ma dostęp do
zasobów

### #4 ⚡ **Cache'owanie**

* W celu zwiększenia wydajności REST API jest cache'owalne

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

### #5 🎭 **Ukrywanie wewnętrznych mechanizmów**

✔️ API powinno być projektowane tak, aby **klient nie wiedział, co dzieje się na serwerze**
✔️ Serwer może wykonywać **dodatkowe akcje**, zanim przygotuje odpowiedź

> 💡 **Korzyści:**
> * 🛡️ **Ochrona danych i infrastruktury organizacji**
> * 🖱️ **Odciążenie urządzenia klienta**

### #6 🛠️ **Code on Demand (opcjonalnie)**

🔹 Możliwość przesyłania fragmentów kodu, które zostaną wykonane **po stronie klienta lub serwera**

***

## 🔍 Warto zobaczyć

👉 **Film:** [Stop Calling Your API a "REST API"](https://www.youtube.com/watch?v=0vC4Xt4wqTk)

---

### ⏭️ Następny rozdział: [08 - Podstawowe metody żądań HTTP a CRUD](08-http-crud.md)  

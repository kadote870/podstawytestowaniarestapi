# 09 - Typy uwierzytelniania w protokole HTTP

## AUTHORIZATION (Autoryzacja) VS. AUTHENTICATION (Uwierzytelnienie)

**Uwierzytelnianie (Authentication)** to proces weryfikacji tożsamości użytkownika lub systemu.
Jest to realizowane poprzez dostarczenie zestawu danych uwierzytelniających, takich jak nazwa
użytkownika i hasło, lub za pomocą certyfikatów cyfrowych lub czynników biometrycznych.

> 💡 Bilet wstępu

**Autoryzacja (Authorization)**, to z drugiej strony, proces określania czy uwierzytelniony
użytkownik lub system posiada odpowiednie uprawnienia do dostępu do określonego zasobu
lub wykonania określonej czynności.

<br>

Innymi słowy, uwierzytelnienie polega na udowodnieniu, kim jesteś, podczas gdy autoryzacja
polega na określeniu, co jesteś uprawniony do zrobienia po uwierzytelnieniu.

<br>

Uwierzytelnienie można porównać do pokazywania dowodu tożsamości przy punkcie
kontrolnym bezpieczeństwa, aby udowodnić swoją tożsamość. Natomiast autoryzacja jest
podobna do udzielenia dostępu do zamkniętej strefy po pokazaniu swojego dowodu
tożsamości.

> 💡 Bilet wstępu + Sprawdzenie wejściówki VIP

* **Uwierzytelnienie** = "Jestem tym, za kogo się podaję."
* **Autoryzacja** = "Mam prawo do tego dostępu."

## Typy uwierzytelniania w protokole HTTP

**Basic Authentication:** Podstawowe uwierzytelnianie to prosty sposób, w którym klient wysyła nazwę
użytkownika i hasło w postaci tekstowej w nagłówku HTTP. Sposób ten jest uważany za mało bezpieczny,
ponieważ dane uwierzytelniające mogą być łatwo przechwycone i odczytane przez osoby niepowołane.

<br>

**ApiKey Authentication:** Polega ona na przekazywaniu unikalnego klucza identyfikacyjnego wraz z
każdym żądaniem do API. Klucz ten jest generowany dla każdego klienta lub aplikacji, co umożliwia
śledzenie i kontrolę dostępu. Używanie klucza API jako formy uwierzytelniania zapewnia prosty sposób
autoryzacji bez konieczności ujawniania wrażliwych danych logowania.

<br>

**Token-based (Bearer) Authentication:** W tym modelu, klient uzyskuje dostęp poprzez uzyskanie tokena
uwierzytelniającego od serwera uwierzytelniania. Token ten jest następnie dołączany do nagłówka
żądania HTTP przy każdym wywołaniu API. W przeciwieństwie do kluczy API, które są stałe I
wykorzystywane do autentykacji aplikacji, tokeny wydawane są dla konktetnego użytkownika,
najczęściej są tymczasowe i wymagają odświeżania po określonym czasie lub po zakończeniu sesji.
Tokeny mogą zawierać różne informacje (JWT), zazwyczaj takie jak: Identyfikator użytkownika,
Uprawnienia dostępu, Data ważności, Dane o użytkowniku etc.

<br>

**Digest Authentication:** poprawia podstawowe uwierzytelnianie poprzez wysłanie
zahashowanej wartości nazwy użytkownika, hasła i innych informacji zamiast tekstu. To
dodaje dodatkową warstwę bezpieczeństwa, ponieważ rzeczywiste dane
uwierzytelniające nie są przesyłane przez sieć. Serwer i klient mają dostęp do
współdzielonego klucza tajnego, aby obliczyć i zweryfikować sumę kontrolną.

<br>

**OAuth Authentication:** OAuth to framework autoryzacji, który umożliwia użytkownikom
udzielenie dostępu do swoich zasobów aplikacjom osób trzecich bez udostępniania
swoich danych uwierzytelniających. Jest powszechnie stosowany przez platformy mediów
społecznościowych i inne usługi internetowe. W przypadku uwierzytelniania OAuth,
użytkownicy uwierzytelniają się przy użyciu dostawcy usługi, a dostawca usługi wydaje
tokeny dostępu autoryzowanym aplikacjom osób trzecich w celu uzyskania dostępu do
określonych zasobów w imieniu użytkownika.

### Następny rozdział: [10 - Endpoint](10-endpoint.md)
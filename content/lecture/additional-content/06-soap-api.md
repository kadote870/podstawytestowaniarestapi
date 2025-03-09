# SOAP API vs REST API

## SOAP API

- **Protokół**: SOAP jest protokołem opartym na XML.

- **Format danych**: Zwykle używa **XML** do wymiany danych, co sprawia, że jest bardziej formalny i złożony w
  porównaniu do innych technologii.
- **Bezpieczeństwo**: Wbudowane mechanizmy bezpieczeństwa (np. **WS-Security**).
- **Transakcje**: Obsługuje **transakcje rozproszone**.
- **Złożoność**: Bardziej formalny i strukturalny, trudniejszy w implementacji.

## REST API

- **Styl architektury**: Opiera się na standardowych metodach HTTP (GET, POST, PUT, DELETE).
- **Format danych**: Obsługuje **JSON**, **XML** i inne formaty.
- **Bezpieczeństwo**: Brak wbudowanych mechanizmów, zależne od SSL/TLS.
- **Prostota**: Bardziej elastyczny, **bezstanowy** i łatwiejszy w użyciu.
- **Skalowalność**: Lepsza wydajność w aplikacjach webowych i mobilnych.

## Kluczowe różnice

- **Protokół vs architektura**: SOAP to **protokół**, REST to **styl architektury**.
- **Format danych**: SOAP używa **XML**, REST obsługuje **JSON** i **XML**.
- **Bezpieczeństwo**: SOAP ma wbudowane mechanizmy bezpieczeństwa, REST nie.
- **Złożoność**: SOAP jest bardziej **skomplikowany**, REST jest **prostszy i bardziej elastyczny**.

## Podsumowanie

- **SOAP**: Użyj, gdy potrzebujesz **wysokiego poziomu bezpieczeństwa** i **transakcji**.
- **REST**: Idealne do **wydajnych aplikacji webowych i mobilnych**, gdy zależy Ci na **prostocie** i **skalowalności**.

```xml
<druzyna_pierscienia>
    <czlonek>
        <imie>Frodo Baggins</imie>
        <rasa>Hobbit</rasa>
        <rola>Nosiciel Pierścienia</rola>
        <charakterystyka>Frodo to młody hobbit z Shire, który staje się nosicielem Jedynego Pierścienia. Jest odważny,
            lojalny i gotów ponieść wielki ciężar odpowiedzialności w misji, by zniszczyć Pierścień.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Samwise Gamgee</imie>
        <rasa>Hobbit</rasa>
        <rola>Wierny towarzysz Froda</rola>
        <charakterystyka>Sam to lojalny i odważny przyjaciel Froda. Jest oddany swojej misji i przyjacielowi, co
            sprawia, że staje się kluczowym wsparciem w podróży.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Aragorn</imie>
        <rasa>Człowiek</rasa>
        <rola>Wojownik i przyszły król</rola>
        <charakterystyka>Aragorn to utalentowany wojownik, który jest prawowitym dziedzicem tronu Gondoru.
            Charakteryzuje się mądrością, odwagą i poczuciem obowiązku.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Gimli</imie>
        <rasa>Krasnolud</rasa>
        <rola>Wojownik</rola>
        <charakterystyka>Gimli to twardy i odważny krasnolud, który od początku wykazuje niechęć do elfów, ale z czasem
            staje się przyjacielem Legolasa. Jest lojalnym członkiem drużyny.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Legolas</imie>
        <rasa>Elf</rasa>
        <rola>Łucznik</rola>
        <charakterystyka>Legolas to elf z Lothlórien, mistrz łucznictwa. Charakteryzuje się wytrzymałością, szybkością i
            dużą wiedzą o naturze. Jest lojalnym i odważnym członkiem drużyny.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Gandalf</imie>
        <rasa>Czarodziej</rasa>
        <rola>Opiekun i doradca</rola>
        <charakterystyka>Gandalf to czarodziej, który pełni rolę mentora i opiekuna drużyny. Jego mądrość, doświadczenie
            i magiczne zdolności pomagają drużynie przetrwać liczne niebezpieczeństwa.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Boromir</imie>
        <rasa>Człowiek</rasa>
        <rola>Wojownik z Gondoru</rola>
        <charakterystyka>Boromir to odważny wojownik, syn Władcy Gondoru. Często zmaga się z pokusą użycia Pierścienia
            do obrony swojego ludu, co prowadzi do tragicznych konsekwencji.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Meriadoc Brandybuck</imie>
        <rasa>Hobbit</rasa>
        <rola>Członek drużyny</rola>
        <charakterystyka>Merry to młodszy hobbit, który przyłącza się do Froda w misji. Z biegiem czasu staje się
            bardziej dojrzały i odważny, uczestnicząc w decydujących momentach.
        </charakterystyka>
    </czlonek>
    <czlonek>
        <imie>Peregrin Took</imie>
        <rasa>Hobbit</rasa>
        <rola>Członek drużyny</rola>
        <charakterystyka>Pippin to zabawny i impulsywny hobbit, który dołącza do drużyny. Choć początkowo wydaje się
            mniej doświadczony, staje się kluczową postacią w trakcie podróży.
        </charakterystyka>
    </czlonek>
</druzyna_pierscienia>

```

```json
{
  "drużyna_pierścienia": [
    {
      "imię": "Frodo Baggins",
      "rasa": "Hobbit",
      "rola": "Nosiciel Pierścienia",
      "charakterystyka": "Frodo to młody hobbit z Shire, który staje się nosicielem Jedynego Pierścienia. Jest odważny, lojalny i gotów ponieść wielki ciężar odpowiedzialności w misji, by zniszczyć Pierścień."
    },
    {
      "imię": "Samwise Gamgee",
      "rasa": "Hobbit",
      "rola": "Wierny towarzysz Froda",
      "charakterystyka": "Sam to lojalny i odważny przyjaciel Froda. Jest oddany swojej misji i przyjacielowi, co sprawia, że staje się kluczowym wsparciem w podróży."
    },
    {
      "imię": "Aragorn",
      "rasa": "Człowiek",
      "rola": "Wojownik i przyszły król",
      "charakterystyka": "Aragorn to utalentowany wojownik, który jest prawowitym dziedzicem tronu Gondoru. Charakteryzuje się mądrością, odwagą i poczuciem obowiązku."
    },
    {
      "imię": "Gimli",
      "rasa": "Krasnolud",
      "rola": "Wojownik",
      "charakterystyka": "Gimli to twardy i odważny krasnolud, który od początku wykazuje niechęć do elfów, ale z czasem staje się przyjacielem Legolasa. Jest lojalnym członkiem drużyny."
    },
    {
      "imię": "Legolas",
      "rasa": "Elf",
      "rola": "Łucznik",
      "charakterystyka": "Legolas to elf z Lothlórien, mistrz łucznictwa. Charakteryzuje się wytrzymałością, szybkością i dużą wiedzą o naturze. Jest lojalnym i odważnym członkiem drużyny."
    },
    {
      "imię": "Gandalf",
      "rasa": "Czarodziej",
      "rola": "Opiekun i doradca",
      "charakterystyka": "Gandalf to czarodziej, który pełni rolę mentora i opiekuna drużyny. Jego mądrość, doświadczenie i magiczne zdolności pomagają drużynie przetrwać liczne niebezpieczeństwa."
    },
    {
      "imię": "Boromir",
      "rasa": "Człowiek",
      "rola": "Wojownik z Gondoru",
      "charakterystyka": "Boromir to odważny wojownik, syn Władcy Gondoru. Często zmaga się z pokusą użycia Pierścienia do obrony swojego ludu, co prowadzi do tragicznych konsekwencji."
    },
    {
      "imię": "Meriadoc Brandybuck",
      "rasa": "Hobbit",
      "rola": "Członek drużyny",
      "charakterystyka": "Merry to młodszy hobbit, który przyłącza się do Froda w misji. Z biegiem czasu staje się bardziej dojrzały i odważny, uczestnicząc w decydujących momentach."
    },
    {
      "imię": "Peregrin Took",
      "rasa": "Hobbit",
      "rola": "Członek drużyny",
      "charakterystyka": "Pippin to zabawny i impulsywny hobbit, który dołącza do drużyny. Choć początkowo wydaje się mniej doświadczony, staje się kluczową postacią w trakcie podróży."
    }
  ]
}
```

### ⏭️ Powrót do: [06 - o API](../06-api.md)

{{ site.data.element.license }}
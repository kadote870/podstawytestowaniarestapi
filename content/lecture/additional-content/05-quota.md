# Quota 📊

Quota to angielskie słowo oznaczające **limit, przydział lub kontyngent**. Może odnosić się do różnych dziedzin, na przykład:

* **📈 W pracy i biznesie** – np. quota sprzedażowa to minimalny cel sprzedażowy, który musi osiągnąć sprzedawca.
* **💻 W IT i usługach online** – oznacza limit zasobów, np. ilości danych, które można pobrać lub wysłać.
* **⚖️ W polityce i prawie** – np. kwoty migracyjne to ograniczenia dotyczące liczby osób mogących osiedlić się w danym kraju.
* **🌍 W handlu międzynarodowym** – kontyngent importowy to maksymalna ilość towarów, które można sprowadzić do kraju.

## Quota w IT 💡

1. **💾 Quota przestrzeni dyskowej**
    * Limit miejsca na dysku, np. użytkownik w chmurze (Google Drive, OneDrive) ma **5 GB** darmowej przestrzeni.

2. **🌐 Quota przepustowości sieciowej**
    * Maksymalna ilość danych, które można przesłać przez sieć w określonym czasie, np. dostawca internetu może nałożyć **limit 500 GB miesięcznie**.

3. **🔗 Quota żądań API**
    * Ograniczenie liczby zapytań do API w danym czasie, np. **Google Maps API** pozwala na **100 000 zapytań miesięcznie** w darmowym planie.

4. **⏳ Quota czasowa**
    * **Quota czasowa** to limit, który określa łączny czas korzystania z usługi w określonym okresie (np. sesja użytkownika lub czas działania procesów).
    * **Przykład:** Darmowy plan chmury pozwala na **50 godzin miesięcznie** działania instancji serwera.
    * **Ważne:** Jeśli czas zostanie przekroczony, może zostać zastosowana blokada dostępu lub wylogowanie użytkownika.

5. **🖥️ Quota zasobów procesora (CPU Quota)**
    * Ograniczenie użycia CPU, np. serwer w chmurze może przydzielić użytkownikowi **maksymalnie 20% mocy obliczeniowej procesora**.

## Quota czasowa to nie timeout ⚠️

**Timeout** (limit czasu wykonania)
* Dotyczy **pojedynczego żądania**.
* Serwer **przerywa operację**, jeśli nie zakończy się w określonym czasie (np. 30 sekund).
* **Przykład:** API zwraca błąd **504 Gateway Timeout**, bo backend nie odpowiedział na czas.

<br>

**Quota czasowa**
* Ogranicza **łączny czas korzystania z usługi** w danym okresie.
* Może dotyczyć **sesji użytkownika** lub **czasu działania procesów**.
* **Przykład:** Darmowy plan chmury pozwala na **50 godzin miesięcznie** działania instancji serwera.
* Jeśli więc serwer przerywa pojedyncze żądanie z powodu długiego przetwarzania, to jest to **timeout**, a nie quota czasowa.

### ⏭️ Powrót do: [05 - Od prostych do złożonych usług internetowych](../05-od-prostych-do-zlozonych-uslug-internetowych.md)
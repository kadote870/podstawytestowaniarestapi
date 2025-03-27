# Test smell: A parasitic energy consumer in software testing

## Information and Software Technology

Volume 181, May 2025

## Authors

* Md Rakib HossainMisu
* Jiawei Li
* Adithya Bhattiprolu
* Yang Liu
* Eduardo Santana de Almeida
* Iftekhar Ahmed

# [LINK](https://www.sciencedirect.com/science/article/pii/S0950584925000102)

## Streszczenie

### Kontekst:

Tradycyjnie badania nad efektywnością energetyczną koncentrowały się na redukcji zużycia energii na poziomie sprzętowym
oraz, w ostatnich latach, na etapie projektowania i kodowania w cyklu życia oprogramowania. Jednak **wpływ testowania
oprogramowania na zużycie energii nie był szeroko analizowany**. W szczególności brak jest badań dotyczących wpływu
jakości projektowania kodu testowego oraz tzw. **test smells (tj. nieoptymalnych wzorców i złych praktyk w kodzie
testowym)** na zużycie energii.

### Cel:
Celem badania jest a**naliza projektów open-source** w celu określenia związku między obecnością test smells a zużyciem
energii podczas testowania oprogramowania.

### Metody:
Przeprowadziliśmy empiryczną analizę mieszaną z dwóch perspektyw:
1. Analizę oprogramowania (eksploracja danych w 12 projektach Apache).
2. Badanie opinii deweloperów (ankieta przeprowadzona wśród 62 praktyków tworzenia oprogramowania).

### Wyniki:
Nasze ustalenia wskazują, że:

1. Test smells mają związek z zużyciem energii w testowaniu oprogramowania – testy zawierające te niepożądane wzorce
zużywają więcej energii niż testy ich pozbawione.
2. Niektóre test smells powodują większe zużycie energii niż inne.
3. Testy poddane refaktoryzacji zużywają mniej energii niż ich pierwotne, obciążone test smells wersje.
4. Większość programistów (45 spośród ankietowanych) nie ma świadomości wpływu test smells na zużycie energii.

###  Wnioski:
Na podstawie wyników podkreślamy konieczność zwiększania świadomości deweloperów na temat wpływu test smells na zużycie
energii. Ponadto przedstawiamy szereg obserwacji, które mogą ukierunkować przyszłe badania i rozwój w tej dziedzinie.
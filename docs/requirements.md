# Wymagania

Wymagania (Requirements) określają, co system powinien robić oraz jakie właściwości i ograniczenia powinien spełniać.

Wymagania powinny być jednoznaczne, zrozumiałe i możliwe do zweryfikowania. Opisujemy oczekiwane zachowanie systemu, a nie sposób jego implementacji.

## Oznaczenia

* **FR** (Functional Requirement) — wymaganie funkcjonalne, określające, co system powinien robić.
* **NFR** (Non-Functional Requirement) — wymaganie niefunkcjonalne, określające, jakie właściwości lub ograniczenia powinien spełniać system.

Każde wymaganie posiada unikalny identyfikator, np. `FR-01` lub `NFR-01`.

## Wymagania funkcjonalne

| ID | Wymaganie |
| :--- | :--- |
| `FR-01` | System automatycznie rejestruje dane telemetryczne przesyłane bezpośrednio z uruchomionego symulatora wyścigowego.  |
| `FR-02` | System umożliwia porównanie dwóch dowolnie wybranych przez gracza okrążeń (np. najlepszego z ostatnim). |
| `FR-03` | System identyfikuje przyczynę straty czasu na podstawie porównania dwóch okrążeń. |
| `FR-04` | System generuje wskazówki dotyczące poprawy czasu okrążenia. |
| `FR-05` | System umożliwia zadawanie pytań w języku naturalnym dotyczących stylu jazdy w wybranej sesji, okrążeniu lub sektorze. |
| `FR-06` | System generuje zalecane ustawienia (setup) dla wybranego samochodu w odpowiedzi na zapytanie gracza określające docelowy tor oraz warunki pogodowe. |
| `FR-07` | System rekomenduje zmiany w ustawieniach samochodu na podstawie opisanego przez gracza problemu z prowadzeniem pojazdu (np. utrata przyczepności, problemy ze skręcaniem, niewłaściwa praca hamulców). |
| `FR-08` | System prezentuje mapę 2D toru z naniesioną linią jazdy gracza. |
| `FR-09` | System umożliwia nałożenie na mapę 2D toru wybranej warstwy wizualnej (heatmapy) prezentującej strefy hamowania lub poziom użycia gazu. |
| `FR-10` | System oznacza na mapie 2D toru miejsca lub sektory, w których gracz miał największą stratę czasu względem najlepszego okrążenia. |
| `FR-11` | System na żądanie gracza analizuje dane treningowe z wybranego okresu czasu i zwraca zestawienie powtarzających się błędów. |
| `FR-12` | System automatycznie grupuje historię sesji na podstawie identyfikatora gracza odczytanego ze strumienia telemetrii. |
| `FR-13` | System prezentuje graczowi dashboard z podsumowaniem jego jazdy: listą zarejestrowanych sesji i okrążeń wraz z czasami, najlepszym okrążeniem na każdym torze i samochodzie oraz zmianą najlepszego czasu okrążenia między kolejnymi sesjami. |

## Wymagania niefunkcjonalne

| ID | Wymaganie |
| :--- | :--- |
| `NFR-01` | System zwraca wyniki analizy powtarzających się błędów z wybranego okresu w czasie nieprzekraczającym 30 sekund dla 95% żądań (przy zakresie danych do 100 okrążeń). |
| `NFR-02` | System zwraca odpowiedź na pojedyncze zapytanie w języku naturalnym (dotyczące stylu jazdy lub ustawień auta) w czasie nieprzekraczającym 10 sekund dla 95% zapytań. |
| `NFR-03` | System renderuje mapę 2D toru wraz z wybraną warstwą heatmapy i znacznikami strat czasu w czasie nieprzekraczającym 2 sekund od wyboru okrążenia. |
| `NFR-04` | Proces rejestracji telemetrii w tle nie powoduje spadku płynności symulatora wyścigowego i zużywa maksymalnie 5% mocy obliczeniowej procesora. |


## Pytania otwarte

* Co system powinien zrobić, jeśli połączenie z symulatorem wyścigowym zostanie przerwane w trakcie trwania sesji lub okrążenia?
* Co system powinien zrobić, jeśli gracz wybierze do porównania okrążenie nieważne?
* Jaka minimalna strata czasu w danym miejscu lub sektorze toru powinna zostać oznaczona na mapie?
* Jakie konkretnie symulatory wyścigowe są wspierane w pierwszej wersji systemu?
* Ile maksymalnie sesji lub okrążeń może obejmować „wybrany okres czasu” podczas analizy powtarzających się błędów?

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
| `FR-02` | System umożliwia porównanie dwóch dowolnie wybranych przez użytkownika okrążeń (np. najlepszego z ostatnim). |
| `FR-03` | System identyfikuje przyczynę straty czasu na podstawie porównania dwóch okrążeń i generuje wskazówki dotyczące poprawy przejazdu. |
| `FR-04` | System umożliwia zadawanie pytań w języku naturalnym dotyczących stylu jazdy w wybranej sesji, okrążeniu lub sektorze i zwraca wygenerowaną odpowiedź. |
| `FR-05` | System generuje zalecane ustawienia samochodu (setup) w odpowiedzi na zapytanie użytkownika określające docelowy tor oraz warunki pogodowe. |
| `FR-06` | System rekomenduje zmiany w ustawieniach samochodu na podstawie opisanego przez użytkownika problemu z prowadzeniem pojazdu (np. utrata przyczepności, problemy ze skręcaniem, niewłaściwa praca hamulców). |
| `FR-07` | System prezentuje mapę 2D toru z naniesioną linią jazdy użytkownika. |
| `FR-08` | System umożliwia nałożenie na mapę 2D toru wybranej warstwy wizualnej (heatmapy) prezentującej strefy hamowania lub poziom użycia gazu. |
| `FR-09` | System oznacza na mapie 2D toru miejsca lub sektory, w których użytkownik popełnił błąd, wraz z krótkim opisem tego błędu. |
| `FR-10` | System na żądanie użytkownika analizuje dane treningowe z wybranego okresu czasu i zwraca zestawienie powtarzających się błędów. |

## Wymagania niefunkcjonalne

| ID | Wymaganie |
| :--- | :--- |
| `NFR-01` | System zwraca wyniki analizy powtarzających się błędów z wybranego okresu w czasie nieprzekraczającym 30 sekund dla 95% żądań (przy zakresie danych do 100 okrążeń). |
| `NFR-02` | System zwraca odpowiedź na pojedyncze zapytanie w języku naturalnym (dotyczące stylu jazdy lub ustawień auta) w czasie nieprzekraczającym 10 sekund dla 95% zapytań. |
| `NFR-03` | System renderuje mapę 2D toru wraz z wybraną warstwą heatmapy i znacznikami błędów w czasie nieprzekraczającym 2 sekund od wyboru okrążenia. |
| `NFR-04` | Proces rejestracji telemetrii w tle nie powoduje spadku płynności gry i zużywa maksymalnie 5% mocy obliczeniowej procesora. |

## Ukryte wymagania
* System automatycznie grupuje historię sesji na podstawie konta gracza z danej gry, odczytanego z danych telemetrycznych.

## Pytania otwarte

* Co system powinien zrobić, jeśli połączenie z symulatorem zostanie przerwane w trakcie trwania sesji lub okrążenia?
* Co system powinien zrobić, jeśli użytkownik wybierze do porównania okrążenie nieważne?
* Jaka minimalna strata czasu w danym punkcie lub sektorze toru jest klasyfikowana przez system jako „błąd” wymagający oznaczenia na mapie?
* Jakie konkretnie gry/symulatory są wspierane w pierwszej wersji systemu?
* Ile maksymalnie sesji lub okrążeń może obejmować „wybrany okres czasu” podczas analizy powtarzających się błędów?

# UC-09 — Przegląd dashboardu

## Aktor

Gracz

## Cel

Szybki przegląd zarejestrowanych sesji, najlepszych okrążeń i postępów w jednym miejscu.

## Powiązane wymagania

FR-13

## Warunek wstępny

Gracz ma zarejestrowaną co najmniej jedną sesję.

## Scenariusz podstawowy

1. Gracz otwiera dashboard.
2. System prezentuje listę zarejestrowanych sesji wraz z okrążeniami i ich czasami.
3. System prezentuje najlepsze okrążenie gracza na każdym torze każdym samochodem.
4. System prezentuje, jak zmieniał się najlepszy czas okrążenia między kolejnymi sesjami.

## Scenariusze alternatywne

- **3a. Brak ważnego okrążenia na danym torze danym samochodem:** System prezentuje sesje bez najlepszego czasu okrążenia i informuje gracza, że nie ma jeszcze ważnego okrążenia.
- **4a. Tylko jedna sesja na danym torze danym samochodem:** System nie prezentuje zmiany najlepszego czasu, ponieważ nie ma jej z czym porównać.

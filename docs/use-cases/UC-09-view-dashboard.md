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

- **3a. Brak ważnych okrążeń na torze:** System prezentuje sesje z tego toru bez wyznaczonego najlepszego okrążenia i bez zmiany czasu między sesjami.
- **4a. Ważne okrążenia tylko z jednej sesji na torze:** System prezentuje najlepsze okrążenie, ale nie wyświetla zmiany czasu między sesjami.

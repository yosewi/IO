# UC-05 — Przegląd mapy toru

## Aktor

Gracz

## Cel

Zobaczenie na mapie toru, jak gracz przejechał okrążenie i w których miejscach stracił najwięcej czasu.

## Powiązane wymagania

FR-08, FR-09, FR-10, NFR-03

## Warunek wstępny

Gracz ma zarejestrowane co najmniej jedno okrążenie.

## Scenariusz podstawowy

1. Gracz wybiera okrążenie do podglądu.
2. System prezentuje mapę 2D toru z naniesioną linią jazdy gracza.
3. System oznacza na mapie miejsca lub sektory, w których gracz miał największą stratę czasu względem najlepszego okrążenia.
4. Gracz wybiera warstwę heatmapy: strefy hamowania lub użycie gazu.
5. System nakłada wybraną warstwę na mapę toru.

## Scenariusze alternatywne

- **1a. Wybrano okrążenie nieważne:** System informuje gracza, że podgląd mapy jest dostępny tylko dla ważnych okrążeń, i prosi o wybranie innego okrążenia.
- **2a. Brak mapy toru:** System informuje gracza, że nie może przedstawić mapy dla tego toru.
- **3a. Wybrane okrążenie jest najlepszym okrążeniem:** System prezentuje mapę bez znaczników straty czasu i informuje gracza, że to jego najlepsze okrążenie.
- **3b. Brak istotnej straty czasu:** System prezentuje mapę bez znaczników straty czasu i informuje gracza, że nie znaleziono miejsc z istotną stratą czasu.
- **3c. Brak najlepszego okrążenia:** System prezentuje mapę bez znaczników straty czasu i informuje gracza, że nie ma jeszcze żadnego ważnego okrążenia na tym torze, z którym można porównać przejazd.

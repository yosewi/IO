# UC-03 — Porównanie okrążenia z najlepszym okrążeniem

## Aktor

Gracz

## Cel

Sprawdzenie, czym wybrane okrążenie różni się od najlepszego okrążenia gracza na danym torze danym samochodem.

## Powiązane wymagania

FR-02, FR-03, FR-04

## Warunek wstępny

Gracz ma zarejestrowane okrążenia na danym torze danym samochodem.

## Scenariusz podstawowy

1. Gracz prosi o porównanie okrążenia z najlepszym, np. „Porównaj moje ostatnie okrążenie z najlepszym”.
2. System ustala najlepsze okrążenie gracza na tym torze tym samochodem.
3. System porównuje okrążenia i wylicza stratę czasu na każdym zakręcie.
4. System wskazuje zakręty, na których gracz stracił najwięcej czasu, i identyfikuje przyczynę straty.
5. System prezentuje wyniki porównania wraz ze wskazówkami, co zmienić.

## Scenariusze alternatywne

- **2a. Brak najlepszego okrążenia:** System informuje gracza, że nie ma jeszcze żadnego ważnego okrążenia na tym torze tym samochodem.
- **2b. Wybrane okrążenie jest najlepszym okrążeniem:** System informuje gracza, że to okrążenie jest jego najlepszym wynikiem.
- **4a. Nie można ustalić przyczyny:** System prezentuje stratę czasu na zakręcie i informuje gracza, że nie udało się ustalić jej przyczyny.

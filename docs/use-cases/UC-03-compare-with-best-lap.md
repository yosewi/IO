# UC-03 — Porównanie okrążenia z najlepszym okrążeniem

## Aktor

Gracz

## Cel

Sprawdzenie, czym wybrane okrążenie różni się od najlepszego okrążenia gracza na danym torze.

## Powiązane wymagania

FR-02, FR-03, FR-04

## Warunek wstępny

Gracz ma zarejestrowane okrążenia na danym torze.

## Scenariusz podstawowy

1. Gracz prosi o porównanie okrążenia z najlepszym, np. „Porównaj moje ostatnie okrążenie z najlepszym”.
2. System ustala najlepsze okrążenie gracza na tym torze.
3. System porównuje okrążenia i wylicza stratę czasu na każdym zakręcie.
4. System wskazuje zakręty, na których gracz stracił najwięcej czasu, i identyfikuje przyczynę straty.
5. System prezentuje wyniki porównania wraz ze wskazówkami, co zmienić.

## Scenariusze alternatywne

- **1a. Wybrano okrążenie nieważne:** System informuje w wynikach, że okrążenie jest nieważne, i nie wyciąga z niego wniosków o błędach jazdy.
- **2a. Brak najlepszego okrążenia:** System informuje gracza, że nie ma jeszcze żadnego ważnego okrążenia na tym torze.
- **2b. Wybrane okrążenie jest najlepszym okrążeniem:** System informuje gracza, że to okrążenie jest jego najlepszym wynikiem.
- **4a. Brak istotnej straty czasu:** System informuje gracza, że wybrane okrążenie nie różni się istotnie od najlepszego na żadnym zakręcie.
- **4b. Nie można ustalić przyczyny:** System prezentuje stratę czasu na zakręcie i informuje gracza, że nie udało się ustalić jej przyczyny.

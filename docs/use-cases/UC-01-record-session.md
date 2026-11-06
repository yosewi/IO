# UC-01 — Rejestracja sesji treningowej

## Aktor

Gracz (aktor główny), Symulator wyścigowy (aktor pomocniczy)

## Cel

Automatyczne zapisanie przejechanej sesji wraz z telemetrią, bez dodatkowych czynności ze strony gracza.

## Powiązane wymagania

FR-01, FR-12, NFR-04

## Warunek wstępny

Symulator wyścigowy jest uruchomiony i udostępnia telemetrię.

## Scenariusz podstawowy

1. Gracz wyjeżdża na tor w symulatorze wyścigowym.
2. System łączy się z symulatorem wyścigowym i zaczyna odbierać telemetrię.
3. System odczytuje identyfikator gracza i dołącza sesję do historii sesji tego gracza.
4. System rejestruje kolejne okrążenia.
5. Gracz kończy jazdę.
6. System zamyka i zapisuje sesję.

## Scenariusze alternatywne

- **2a. Symulator wyścigowy nie udostępnia telemetrii:** System informuje gracza, że nie odbiera danych, i wskazuje, że należy włączyć udostępnianie telemetrii w ustawieniach symulatora wyścigowego.
- **3a. Nieznany identyfikator gracza:** System rozpoczyna nową historię sesji dla tego gracza.
- **4a. Połączenie z symulatorem wyścigowym zostało przerwane:** System zapisuje okrążenia ukończone przed przerwaniem, a przerwane okrążenie oznacza jako nieważne.

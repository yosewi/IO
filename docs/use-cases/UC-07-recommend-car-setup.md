# UC-07 — Dobór ustawień samochodu pod tor i pogodę

## Aktor

Gracz

## Cel

Otrzymanie zalecanych ustawień dla wybranego samochodu na konkretny tor i warunki pogodowe.

## Powiązane wymagania

FR-06, NFR-02

## Warunek wstępny

System posiada informacje o torach, samochodach i ustawieniach samochodu, które gracz może zmieniać.

## Scenariusz podstawowy

1. Gracz prosi o ustawienia samochodu, np. „Przygotuj setup McLarena na Spa na deszcz”.
2. System dobiera ustawienia samochodu pod tor i warunki pogodowe.
3. System prezentuje zalecane ustawienia wraz z krótkim uzasadnieniem.

## Scenariusze alternatywne

- **2a. Nie podano samochodu, toru lub warunków pogodowych:** System prosi gracza o uzupełnienie brakujących informacji.
- **2b. Nieznany samochód lub tor:** System informuje gracza, że nie posiada informacji o wskazanym samochodzie lub torze.

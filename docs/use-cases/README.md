# Przypadki użycia


## Wersja Mermaid


### 1. Aktor i przypadek użycia

```mermaid
flowchart LR
    Gracz["Gracz"]
    UC02(["Porównanie dwóch okrążeń"])

    Gracz --- UC02
```


### 2. Granice systemu i generalizacja

```mermaid
flowchart LR
    Gracz["Gracz"]
    Sym["Symulator wyścigowy"]

    subgraph System["SimWall"]
        UC01(["UC-01<br/>Rejestracja sesji treningowej"])
        UC02(["UC-02<br/>Porównanie dwóch okrążeń"])
        UC03(["UC-03<br/>Porównanie okrążenia z najlepszym okrążeniem"])
        UC04(["UC-04<br/>Pytanie o styl jazdy"])
        UC05(["UC-05<br/>Przegląd mapy toru"])
        UC06(["UC-06<br/>Analiza powtarzających się błędów"])
        UC07(["UC-07<br/>Dobór ustawień samochodu pod tor i pogodę"])
        UC08(["UC-08<br/>Korekta ustawień na podstawie problemu z prowadzeniem"])
        UC09(["UC-09<br/>Przegląd dashboardu"])
    end

    Gracz --- UC01
    Gracz --- UC02
    Gracz --- UC03
    Gracz --- UC04
    Gracz --- UC05
    Gracz --- UC06
    Gracz --- UC07
    Gracz --- UC08
    Gracz --- UC09

    UC01 --- Sym

    UC03 -->|generalizacja| UC02
```


## Wersja PlantUML — zgodna z notacją UML


### 1. Aktor i przypadek użycia

```plantuml
@startuml
actor Gracz
usecase "Porównanie dwóch okrążeń" as UC02
Gracz --> UC02
@enduml
```


### 2. Granice systemu i generalizacja

```plantuml
@startuml
left to right direction

actor Gracz
actor "Symulator wyścigowy" as Sym

rectangle "SimWall" {
    usecase "UC-01\nRejestracja sesji treningowej" as UC01
    usecase "UC-02\nPorównanie dwóch okrążeń" as UC02
    usecase "UC-03\nPorównanie okrążenia\nz najlepszym okrążeniem" as UC03
    usecase "UC-04\nPytanie o styl jazdy" as UC04
    usecase "UC-05\nPrzegląd mapy toru" as UC05
    usecase "UC-06\nAnaliza powtarzających się błędów" as UC06
    usecase "UC-07\nDobór ustawień samochodu\npod tor i pogodę" as UC07
    usecase "UC-08\nKorekta ustawień na podstawie\nproblemu z prowadzeniem" as UC08
    usecase "UC-09\nPrzegląd dashboardu" as UC09
}

Gracz -- UC01
Gracz -- UC02
Gracz -- UC03
Gracz -- UC04
Gracz -- UC05
Gracz -- UC06
Gracz -- UC07
Gracz -- UC08
Gracz -- UC09

UC01 -- Sym

UC03 --|> UC02

@enduml
```


## Katalog przypadków użycia

| ID | Przypadek użycia | Aktor | Wymagania |
|----|------------------|-------|-----------|
| [UC-01](UC-01-record-session.md) | Rejestracja sesji treningowej | Gracz, Symulator wyścigowy | FR-01, FR-12, NFR-04 |
| [UC-02](UC-02-compare-laps.md) | Porównanie dwóch okrążeń | Gracz | FR-02, FR-03, FR-04 |
| [UC-03](UC-03-compare-with-best-lap.md) | Porównanie okrążenia z najlepszym okrążeniem | Gracz | FR-02, FR-03, FR-04 |
| [UC-04](UC-04-ask-about-driving-style.md) | Pytanie o styl jazdy | Gracz | FR-05, NFR-02 |
| [UC-05](UC-05-view-track-map.md) | Przegląd mapy toru | Gracz | FR-08, FR-09, FR-10, NFR-03 |
| [UC-06](UC-06-analyze-recurring-mistakes.md) | Analiza powtarzających się błędów | Gracz | FR-11, FR-04, NFR-01 |
| [UC-07](UC-07-recommend-car-setup.md) | Dobór ustawień samochodu pod tor i pogodę | Gracz | FR-06, NFR-02 |
| [UC-08](UC-08-fix-handling-problem.md) | Korekta ustawień na podstawie problemu z prowadzeniem | Gracz | FR-07, NFR-02 |
| [UC-09](UC-09-view-dashboard.md) | Przegląd dashboardu | Gracz | FR-13 |

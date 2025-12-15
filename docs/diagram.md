# dookołaSchemat działania aplikacji

Poniżej znajduje się uproszczony przepływ użytkownika w aplikacji (User Flow).

```mermaid
graph TD;
    Start([Start Aplikacji]) --> Logowanie{Zalogowany?};
    Logowanie -- Nie --> EkranLogowania[Ekran Logowania];
    EkranLogowania --> Walidacja[Weryfikacja danych];
    Walidacja --> Logowanie;
    Logowanie -- Tak --> Dashboard[Pulpit Główny];
    
    Dashboard --> ListaZadan[Lista Zadań];
    Dashboard --> Kalendarz[Kalendarz];
    
    ListaZadan --> Dodaj[Dodaj / Edytuj Zadanie];
    Kalendarz --> Podglad[Podgląd Dnia];
    
    Dodaj --> Zapisz[(Zapisz w Bazie)];
    Zapisz --> Dashboard;
    
    Dashboard --> Koniec([Wyloguj / Wyjście]);
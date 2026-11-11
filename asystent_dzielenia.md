# 🤖 Projekt: Cyfrowy Asystent Dzielenia Pisemnego
*Dokumentacja techniczna i plan pracy dla dewelopera: Bata (Bartek)*
*Architekt i Mentor: Tata (Tech Leader)*

Witaj w zespole! Przed Tobą ważne zadanie. Tworzymy program, który pomoże dzieciom zrozumieć dzielenie pisemne. Pracujemy profesjonalną metodą projektową (Agile/Scrum). Całe zadanie dzielimy na niezależne Sprinty. 

W tym Sprincie budujemy wyłącznie czysty "silnik matematyczny" (backend). Nie rysujemy grafiki, nie klonujemy kratek. Program ma działać w pamięci komputera na bazie list i zmiennych.

---

## 🏃 SPRINT 1: MÓZG MATEMATYCZNY (Logika Silnika)

### 📋 Lista zadań do zrobienia (Do wrzucenia na tablicę Kanban):

- [ ] Task 1.1: Inicjalizacja Zmiennych i Struktur Danych (Listy)
- [ ] Task 1.2: Rozbicie liczby wejściowej na pojedyncze cyfry
- [ ] Task 1.3: Główna pętla matematyczna algorytmu dzielenia
- [ ] Task 1.4: Testy jednostkowe (Bug-hunting dla różnych liczb)

---

## 🛠️ Specyfikacja Techniczna i Architektura (Jak to zakodować)

### 1. Wymagane struktury danych (Stwórz w Scratchu):
*   `Lista_Dzielna` — tu komputer rozbije wpisaną przez użytkownika liczbę (np. indeks 1: `1`, indeks 2: `4`, indeks 3: `5` dla liczby 145).
*   `Lista_Wynik` — pusta lista, do której Twój algorytm będzie doklejał kolejne cyfry wyniku.
*   Zmienna `Bieżąca_Wartość` — Twój roboczy numer, z którego aktualnie wydzielasz pełne cyfry.
*   Zmienna `Dzielnik` — liczba, przez którą dzielimy.
*   Zmienna `Indeks` — licznik pętli (od 1 do długości Listy_Dzielnej).

### 2. Logika głównego algorytmu krok po kroku:
1. Zapytaj użytkownika o Dzielną (np. 145) i Dzielnik (np. 4).
2. Wyczyszczaj obie listy przed każdym nowym uruchomieniem.
3. Przepisz pętlą tekst Dzielnej do `Lista_Dzielna` (każda cyfra to osobny wiersz).
4. Ustaw `Bieżąca_Wartość` na 0, a `Indeks` na 1.
5. **Uruchom pętlę (powtórz tyle razy, ile jest cyfr w `Lista_Dzielna`):**
    *   `Bieżąca_Wartość` = (Stara wartość zmiennej `Bieżąca_Wartość` * 10) + (wartość z `Lista_Dzielna` pod numerem `Indeks`).
    *   Oblicz, ile razy `Dzielnik` mieści się w `Bieżąca_Wartość` i dodaj tę cyfrę na koniec `Lista_Wynik` (Wskazówka: użyj zaokrąglenia w dół: `zaokrąglij w dół (Bieżąca_Wartość / Dzielnik)`).
    *   Ustaw nową `Bieżąca_Wartość` jako resztę z tego dzielenia (Wskazówka: `Bieżąca_Wartość` - (ostatnia dodana cyfra wyniku * `Dzielnik`)).
    *   Zmień `Indeks` o 1, aby przejść do kolejnej cyfry.

---

## 🧪 Scenariusze Testowe (Sprawdź swój kod!)
Po zakodowaniu silnik musi bezbłędnie podawać wyniki w `Lista_Wynik` dla poniższych przypadków:
1.  `145 ÷ 4` -> Wynik w liście: `0, 3, 6` (co oznacza 36), Reszta końcowa = `1`.
2.  `912 ÷ 3` -> Wynik w liście: `3, 0, 4` (co oznacza 304), Reszta końcowa = `0`.

Zgłaszaj gotowość do przeglądu kodu (Code Review) po zaliczeniu testów! Powodzenia!

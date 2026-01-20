# Model_bias_LLM

## PLAN PLIKÓW: (w kolejności działania)
* candidates_generator.ipynb -> generator profili
* candidates.json -> profile stworzone przez powyższy kod

* model_answer_generator.ipynb -> generator odpowiedzi modelów
* bias_audit_results_full.csv -> pełne, finałowe odpowiedzi modelu
* bias_results_partial.csv -> plik pomocniczy którego używaliśmy, żeby na pewno nie stracić pracy gdyby kod siadł
* analyze_bias.ipynb -> plik z analizą i wizualizacją wygenerowanych danych
* prezentacja.pdf -> prezentacja wyników
* rapot.pdf -> końcowy raport techniczny



## NASZE ZADANIE:
11. Analiza biasu LLM w scenariuszach rekrutacyjnych

**Cel:**
Zbadać, czy i jak LLM wykazuje uprzedzenia (bias) przy ocenie fikcyjnych CV / kandydatów.

**Zakres (minimalny):**
* Przygotować zestaw profili kandydatów (syntetycznych), w których zmieniane są np. imię, płeć, narodowość/globalny kontekst przy zachowaniu tych samych kwalifikacji.
* LLM ocenia „dopasowanie do stanowiska” / nadaje punktową ocenę.
* Porównać wyniki między wersjami różniącymi się tylko cechą wrażliwą.

**Warstwa wyjaśnialności:**
* wyjaśnienia, na które elementy CV model się powołuje,
* raport z wizualizacją różnic (wykresy, tabelki).


## OFICJALNE ZAŁOŻENIA PROJEKTU:
W każdym projekcie zespół powinien:

**1. Zdefiniować zadanie i dane**
* Przygotować / dobrać min. 50–100 przykładów (promptów) z ręcznie nadanymi etykietami / oczekiwanymi odpowiedziami lub ocenami.
* Zwięźle opisać domenę (co model ma robić i dla kogo).

**2. Zbudować pipeline z LLM**
* Wybrać 1–2 modele (API lub open-source).
* Zaprojektować prompt(y), ew. prosty RAG (retrieval-augmented generation).

**3. Przeprowadzić ewaluację**
* Zdefiniować 1–2 proste metryki jakości (accuracy, F1, zgodność z etykietą, ocena ekspercka itp.).
* Porównać co najmniej dwa warianty (np. inne prompty, inny model, dodatkowy kontekst).

**4. Dodać warstwę wyjaśnialności**
* Co najmniej jedna z opcji:
  - podświetlanie ważnych fragmentów tekstu,
  - wizualizacja użytych dokumentów (dla RAG),
  - chain-of-thought (rozumowanie krok po kroku),
  - self-critique / auto-ocena odpowiedzi,
  - LLM jako generator opisowych wyjaśnień dla użytkownika.

**5. Przygotować raport i krótkie demo**
* Opis zadania, metody, wyników, ograniczeń.
* 5–10 ciekawych przykładów: „success case” + „failure case” z komentarzem.

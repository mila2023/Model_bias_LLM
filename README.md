# Model_bias_LLM

## PLAN DZIAŁANIA:

* Zbiór 100 przykładów - 50 par kandydatów, z cechami i score, różniącymi się jedną cechą wrażliwą, info gdzie się rekrutują
* Zaprojektowanie systemu promptów, który wymusza dodatkowo konkretny format odpowiedzi i podczepienie do llma (gpt-3.5-turbo, gemini-1.5-flash, Llama-3 - trzeba zrobić research co wybrać)
* Warianty: model 1 vs model 2, lub jeden model z dwoma różnymi promptami, np aby zwracał uwagę tylko na skillsy techniczne/ miękkie
* Metryka: Bias Score - różnica w średniej ocenie między grupami przy tych samych kwalifikacjach
* Najlepsze dla nas:
  Chain-of-Thought (CoT): Prosisz model: "Przeanalizuj CV krok po kroku, wypisz plusy, minusy, a na końcu daj ocenę".
  SHAP (Podświetlanie fragmentów): To pokaże, które słowa (np. "Anna", "Harvard", "Python") wpłynęły na ocenę.
* Prezentacja (Raport i Demo): ja bym powiedziała trzymajmy się formatu prezentacji, jeden slajd o problemie, kilka o sposobie budowania promptów i kilka przykładowych CV z ich formatem. Potem do tego 5-10 CV i success/ failure case-y z komentarzami i potem metryki, nasza Bias Score którą zwracał model vs ta którą my nadaliśmy i dwie z listy: Chain-of-Thought i SHAP.


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

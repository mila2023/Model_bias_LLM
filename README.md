# Model_bias_LLM

Plan działania:

* Zbiór 100 przykładów - 50 par kandydatów, z cechami i score, różniącymi się jedną cechą wrażliwą, info gdzie się rekrutują
* Zaprojektowanie systemu promptów, który wymusza dodatkowo konkretny format odpowiedzi i podczepienie do llma (gpt-3.5-turbo, gemini-1.5-flash, Llama-3 - trzeba zrobić research co wybrać)
* Warianty: model 1 vs model 2, lub jeden model z dwoma różnymi promptami, np aby zwracał uwagę tylko na skillsy techniczne/ miękkie
* Metryka: Bias Score - różnica w średniej ocenie między grupami przy tych samych kwalifikacjach
* Najlepsze dla nas:
  Chain-of-Thought (CoT): Prosisz model: "Przeanalizuj CV krok po kroku, wypisz plusy, minusy, a na końcu daj ocenę".
  SHAP (Podświetlanie fragmentów): To pokaże, które słowa (np. "Anna", "Harvard", "Python") wpłynęły na ocenę.
* Prezentacja (Raport i Demo): ja bym powiedziała trzymajmy się formatu prezentacji, jeden slajd o problemie, kilka o sposobie budowania promptów i kilka przykładowych CV z ich formatem. Potem do tego 5-10 CV i success/ failure case-y z komentarzami i potem metryki, nasza Bias Score którą zwracał model vs ta którą my nadaliśmy i dwie z listy: Chain-of-Thought i SHAP.

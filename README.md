| Sekcja | Opis |
|---|---|
| Tytuł projektu | Travel Planer |
| Lista osób zaangażowanych | Michał Rajkowski (248821)<br>Michał Bernacki-Janson (**indeks**)<br>Mateusz Zbrocki (**indeks**)<br>Julianna Godziszewska (263841) |
| One-liner — cel projektu | Stworzenie planera wycieczek AI |
| Krótki opis (max ½ A4) | Rozbudowany wieloagentowy RAG, który potrafi zaplanować wycieczkę z użytkownikiem (na bazie rozmowy w języku naturalnym) i wykorzystać do tego zarówno dane przestrzenne (punkty zainteresowań na mapie, trasy) jak i ceny, cechy atrakcji. <br><br> Dodatkowo asystent uwzględnia w zwróconych trasach preferencje semantyczne użytkownika. <br><br> System wykorzystuje wiele baz wiedzy odnośnie punktów turystycznychi wrocławia, dane OSM, opisy stron internetowych powiązane z atrakcjami, jak i posiada dostęp do API w celu weryfikacji aktualnych danych.|
| Grafika (opcjonalna) | TODO: Diagram ilustrujący projekt, flow przetwarzania, zrzut ekranu z dema |
| Problemy IP | TODO: Jakie problemy związane z własnością intelektualną zauważacie już w projekcie? Każda osoba wpisuje jedną: 1. @imie.nazwisko ... <br> 1. @Michał.Rajkowski : Scrapowanie stron internetowych / wyłuskiwanie informacji ze stron do naszej bazy wiedzy.<br> 2. @Julianna.Godziszewska : Naruszenie polityki użycia API -Niedozwolone i trwałe buforowanie danych w bazie wiedzy (np. TripAdvisor) lub obowiązek ich cyklicznego usuwania i odświeżania (np. max 30 dni w przypadku GoogleMaps). <br> 3. <br> 4.|
| Wyzwania etyczne/społeczne | TODO: Czy widzicie potencjalne wyzwania etyczne lub społeczne w Waszym projekcie? (AI Act, dane osobowe, generowanie treści, itp.) |


Prompty do chatów:

- "(przeklejenie całej tabelki z opisami) Jakie mogą być ogólne problemy z własnością intelektualną w projektach tego typu?"
- "Podaj mi przykłady API (które mozemy wykorzystać w naszym projekcie), które mają rygorystyczne zasady dotyczące cachowania danych.

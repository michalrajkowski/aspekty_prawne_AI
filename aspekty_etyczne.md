Aspekty etyczne (15 pkt)
Jedna spójna sekcja obejmująca cztery wymiary etyczne Waszego projektu:

- Przejrzystość — gdzie i do czego korzystacie z AI? Co jest automatyczne, a gdzie jest człowiek w pętli? Co udostępniacie (kod, dane, wyniki)?
- Wyjaśnialność — jakie problemy etyczne mogą się pojawić (dyskryminacja, prywatność, niesprawiedliwe decyzje)? Jak im zapobiegacie?
- Inkluzywność — wpływ na rynek pracy, potencjalna dyskryminacja, jakość i pokrycie danych.
- Wyrównanie (alignment) — zgodność z ramami prawnymi (RODO, AI Act, prawo autorskie, regulacje branżowe).

---

## Przejrzystość
- **Wykorzystanie AI:**
  - Sztuczna inteligencja jest wykorzystywana do przetwarzania języka naturalnego (konwersacje z użytkownikiem poprzez LLM, ekstrakcja wymagań użytkownika, wyszukiwanie wektorowe z bazy wiedzy).
  - Automatycznie odbywają się zapytania do API (OSM) oraz układanie harmonogramu wycieczki wraz z optymalizacją tras z uwzględnieniem odległości i czasu.
- **Człowiek w pętli:** System ma charakter doradczy, co oznacza, że ostetczną decyzję odnośie planu oraz elementów wycieczki dokonuje użytkownik, który może narzucic swoje wybory systemowi. Wszelkich rezerwacji biletów itp. użytkonik musi tez sam dokonać.
- **Udostępnianie:** Dla potencjalnych klientów udostepniamy zarówno kod jak i bazę wiedzy (zbiór danych). Natomiast użytkownik końcowy korzysta wyłącznie z interfejsu systemu i nie ma wglądu ani w kod, ani bezpośrednio w zbiór danych. Udostepnione także będą wyniki ewaluacji na zbiorze testowym, aby potencjalni klienci mogli zobaczyć, że system w rzeczywistości działa.

## Wyjaśnialność
- **Zidentyfikowane ryzyka:**
  - Halucynacje modeli językowych - LLM mógłby polecić nieistniejące już restauracje, czy niezaktualizowane godiny otwarcia atrakcji. Z tego względu zdecydowalismy się na wykorzystanie systemu RAG, w którym LLM korzysta z bazy wiedzy, która jest na bieżąco aktualizowana o najnowsze informacje. Dodatkowo model językowy po zaproponowaniu jakiejs atrakcji poweinien powołać się na nią i podac np. link do jej oficjalnej strony, tak aby użytkownik mógł sprawdzić aktualność danych z oficjalnymi źródłami.
  - Opóźnienia - Multi-agentowe frameworki są wolne, ponieważ agenty uszą się ze sobą komunikować i wykonywać wszytskie powierzone im zadania, przez co ygenerowanie planu dla użytkownika może potrwać dłuższą chwilę. Rozwiązaniem jest asynchroniczność Komunikatora, która polega na tym, że komunikator daje informacje wzwrotną użytownikowi podczas tworzenia planu, tak żeby został on poinformowany, że proces jest w toku + żeby zająć czymś użytkownika (np. "Jasne, szukam najlepszych opcji. Widzę fajną pizzerię blisko Rynku, daj mi chwilę na ułożenie trasy...").
  - Brak transparentności procesu decyzyjnego - Przykłądowo użytkownik prosi o 5 atrakcji, a system zwraca tylko 3. Użytkownik traci zaufanie do systemu, ponieważ nie zwrócił mu w pełni zgodnej odpoweidzi z jego pytaniem. Z tego względu system powinien "myśleć na głos" i informować o wszytskich swoich decyzjach użytkownika (np. "Znalazłem 5 atrakcji, ale ustaliłem, że fizycznie zdążysz odwiedzić tylko 3 przed zamknięciem, dlatego odrzuciłem dwie z nich").

## Inkluzywność
- **Wpływ na rynek pracy:** - Asystent nie ma na celu zastąpienia licencjonowanych przewodników. Narzędzie automatyzuje żmudny proces planowania, wspierając turystykę niezależną. System może różniez służyć jako narzędzie wspomagające dla klientów biur podróży lub promować konkretne atrakcje, restauracje itd. (w zależności od budowy bazy wiedzy).
- **Potencjalna dyskryminacja:** - Pomijanie niektórych atrakcji lub miejsc (np. nie polecanie użytkownikowi jednej kawiarni, która idealnie pasowałaby do planu, ze względu na brak informacji o niej w bazie danych lub celowe nieuwzględnienie jej w bazie danych - jeżeli dana atrakcja nie ma swojej strony internetowej lub nie wyświetla się na mapach google to mogła zostać pominięta podczas scrapowania danych lub zostało zebranych o niej bardzo niewiele informacji). Agent RAG powinien uzywać najpierw tagów z OSM do wyszukiwania pasujących miejsc i atrakcji, a dopiero później wzbogacać je o opisy semantyczne, żeby nie dyskryminować punktów bez długich artykułów w sieci.
- **Jakość, pokrycie i aktualność danych** - Dane turystyczne mogą się starzeć, przez co stają się nieaktualne. Bardzo ważna jest cykliczna aktualizacja wektorowej bazy wiedzy (np. poprzez zautomatyzowane, okresowe wywoływanie skryptów scrapujących i weryfikację z API OSM), dzięki czemu asystent zawsze operuje na świeżych i sprawdzonych informacjach.

## Wyrównanie
- **RODO:**
  - System aktywnie buduje profile turystyczne, na stałe przechowując preferencje użytkowników (np. alergie, ulubione typy atrakcji) pozyskane z promptów. - Użytkownik wyraża świadomą zgodę na zapisywanie preferencji i w każdej chwili za pomocą jednego kliknięcia ma prawo do usunięcia swojego konta i historii konwersacji (realizacja prawa do bycia zapomnianym).
  - Istnieje ryzyko pobrania przypadkowych danych osobowych, np. podczas scrapowania opinii podczas tworzenia lub aktualizowania bazy wiedzy RAG. - Wprowadzamy filtry oczyszczające recenzje z danych osobowych przed dodaniem ich do wektorowej bazy (minimalizacja danych). 
- **AI Act:** Zgodnie z unijnym rozporządzeniem, nasz Asystent kwalifikuje się jako system ograniczonego ryzyka (chatbot w domenie niezagrażającej życiu ani zdrowiu). Spełniamy wszystkie wymogi poprzez jasne znakowanie, że użytkownik wchodzi w interakcję z maszyną. System informuje przy powitaniu, że nie jest prawdziwym człowiekiem, a maszyną. Dodatkowo każda wygenerowana trasa zawiera zastrzeżenie, że opiera się na rekomendacjach AI, a użytkownik musi wziąć poprawkę na czynniki losowe (aktualność cen, nagłe remonty, pogodę), które mogły ulec zmianie w świecie rzeczywistym.
- **Prawo Autorskie:** Ryzyko skopiowania cudzych, twórczych treści (np. całych artykułów z blogów). Nasza baza wiedzy powinna zawierać tylko surowe informacje i fakty, które nie podlegają prawu autorskiemu.

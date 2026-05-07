AI Act (15 pkt)
Klasyfikacja ryzyka Waszego systemu AI wg AI Act (niedopuszczalne / wysokie / ograniczone / minimalne) — uzasadnienie.
Jakie obowiązki wynikają z tej klasyfikacji dla Waszego projektu?
Czy Wasz system podlega dodatkowym wymaganiom (np. transparentność dla modeli generatywnych, GPAI)?
Co musielibyście zmienić w projekcie, żeby spełnić wymagania AI Act?

---
## Klasyfikacja ryzyka systemu wg AI Act

**Ryzyko niedopuszczalne:**  
Ta kategoria nie ma zastosowania, ponieważ nasz Travel Planner nie służy do manipulacji użytkownikiem, scoringu społecznego, identyfikacji biometrycznej ani wykorzystywania podatności osób. System ma charakter doradczy i planistyczny, a jego celem jest pomoc w organizacji wycieczki.

**Ryzyko wysokie:**  
Ta kategoria również nie ma zastosowania, ponieważ system nie podejmuje decyzji w obszarach takich jak edukacja, zatrudnienie, kredyty, dostęp do usług publicznych, migracja, egzekwowanie prawa czy infrastruktura krytyczna. Rekomendacje tras i atrakcji nie mają skutku prawnego ani nie decydują o istotnych uprawnieniach użytkownika.

**Ryzyko minimalne:**  
Część funkcji technicznych, takich jak filtrowanie atrakcji, wyszukiwanie punktów POI czy obliczanie tras, może mieć charakter minimalnego ryzyka. Nie jest to jednak właściwa klasyfikacja całego systemu, ponieważ projekt wykorzystuje konwersacyjny interfejs AI i generuje spersonalizowane odpowiedzi.

**Ryzyko ograniczone:**  
Najbardziej właściwą klasyfikacją dla całego systemu jest ryzyko ograniczone. Travel Planner działa jako chatbot/asystent AI, który rozmawia z użytkownikiem w języku naturalnym, interpretuje jego preferencje i generuje propozycje planów wycieczek. Z tej klasyfikacji wynikają przede wszystkim obowiązki transparentności dla systemów wchodzących w bezpośrednią interakcję z osobą fizyczną, opisane w art. 50 AI Act. Użytkownik powinien być jasno poinformowany, że rozmawia z systemem AI, a wygenerowany plan jest rekomendacją, nie gwarancją poprawności ani aktualności danych. System powinien także komunikować ograniczenia dotyczące cen, godzin otwarcia, dostępności atrakcji, remontów, warunków pogodowych i jakości danych źródłowych.

## Obowiązki transparentności i GPAI

Tak, system podlega dodatkowym wymaganiom transparentności, ponieważ działa jako chatbot/asystent AI i generuje treści dla użytkownika.

- **art. 50 ust. 1 AI Act** — fragment: „interacting with an AI system”. Przepis dotyczy systemów AI przeznaczonych do bezpośredniej interakcji z osobami fizycznymi i obowiązku poinformowania użytkownika, że wchodzi w interakcję z AI. W naszym projekcie oznacza to widoczny komunikat przed pierwszą interakcją, np. „Rozmawiasz z asystentem AI”.
- **art. 50 ust. 2 AI Act** — fragment: „machine-readable format”. Przepis dotyczy oznaczania wyników systemów generujących syntetyczne treści audio, obraz, wideo lub tekst jako wygenerowanych albo zmanipulowanych przez AI, o ile jest to technicznie wykonalne. W naszym projekcie oznacza to opisanie planów wycieczek, opisów tras i rekomendacji jako treści generowanych automatycznie, a przy eksporcie dodanie prostego znacznika/metadanych, np. `generated_by_ai: true`.
- **art. 50 ust. 3 AI Act** — fragment: „emotion recognition system” oraz „biometric categorisation system”. Ten punkt nie dotyczy naszego projektu, bo Travel Planner nie rozpoznaje emocji użytkownika i nie dokonuje kategoryzacji biometrycznej.
- **art. 50 ust. 4 AI Act** — fragment: „deep fake” oraz „informing the public”. Ten punkt nie dotyczy standardowej rozmowy z użytkownikiem ani prywatnie generowanego planu wycieczki. Mógłby mieć znaczenie dopiero wtedy, gdybyśmy publicznie publikowali wygenerowane przez AI teksty informacyjne, np. publiczne przewodniki, artykuły lub opisy atrakcji, albo generowali obrazy/audio/wideo typu deepfake. W takim wariancie należałoby jawnie oznaczyć treść jako wygenerowaną lub zmanipulowaną przez AI.
- **art. 50 ust. 5 AI Act** — fragment: „clear and distinguishable manner”. Przepis wskazuje, że informacje z art. 50 powinny być podane jasno, rozpoznawalnie i najpóźniej przy pierwszej interakcji lub pierwszej ekspozycji. Dlatego komunikat o AI nie powinien być ukryty wyłącznie w regulaminie; powinien być widoczny w interfejsie.
- **art. 50 ust. 6–7 AI Act** — te ustępy nie dodają dla naszego prototypu osobnego obowiązku funkcjonalnego. Ust. 6 wskazuje, że obowiązki z art. 50 nie uchylają innych obowiązków, np. dla systemów wysokiego ryzyka, a ust. 7 dotyczy prac AI Office nad kodeksami dobrych praktyk dla wykrywania i oznaczania treści AI.

W zakresie GPAI główne obowiązki dotyczą przede wszystkim dostawców modeli ogólnego przeznaczenia, np. dostawców API LLM albo twórców modeli open-weight, a nie zespołu budującego aplikację korzystającą z takich modeli.

- **art. 53 AI Act** — fragment: „technical documentation of the model”. Przepis nakłada na dostawców modeli GPAI obowiązki dotyczące dokumentacji technicznej, informacji dla integratorów, polityki zgodności z prawem autorskim i publicznego streszczenia danych treningowych. Dla nas oznacza to, że powinniśmy dokumentować, z jakich modeli korzystamy, i wybierać dostawców, którzy publikują wymagane informacje.
- **art. 54 AI Act** — fragment: „authorised representative”. Przepis dotyczy głównie upoważnionych przedstawicieli dostawców GPAI spoza UE. Dla naszego projektu to warunek pośredni przy wyborze dostawcy modelu, a nie bezpośredni obowiązek zespołu.
- **art. 55 AI Act** — fragment: „systemic risks”. Przepis dotyczy dodatkowych obowiązków dostawców modeli GPAI z ryzykiem systemowym, m.in. ewaluacji modelu, ograniczania ryzyk systemowych, raportowania poważnych incydentów i cyberbezpieczeństwa. Nie zakładamy, że jesteśmy takim dostawcą, ale przy użyciu takich modeli powinniśmy sprawdzić deklaracje zgodności dostawcy.

## Plan zmian P0/P1/P2

**P0 — transparentność w interfejsie:**  
Dodać banner lub komunikat przed pierwszą interakcją: „Rozmawiasz z systemem AI”. Oznaczać wygenerowany plan jako rekomendację, a nie oficjalną lub gwarantowaną informację. Dodać krótkie ostrzeżenie, że ceny, godziny otwarcia, dostępność atrakcji, remonty, pogoda i przebieg tras mogą być nieaktualne.

**P1 — bezpieczeństwo promptów i odpowiedzi (etap docelowy, nie minimum prototypu):**  
W przypadku naszego systemu ograniczonego ryzyka AI Act wymaga przede wszystkim transparentności z art. 50, więc w wersji prototypowej za minimum uznajemy P0: jasną informację, że treść jest generowana przez AI i może być błędna albo nieaktualna. Pełny filtr promptów oraz odpowiedzi traktujemy jako kolejny etap bezpieczeństwa przed produkcyjnym wdrożeniem lub publicznym udostępnieniem: powinien ograniczać treści niebezpieczne, nielegalne, naruszające prywatność lub wprowadzające w błąd. Taki filtr może też wynikać z warunków użycia dostawcy modelu albo Acceptable Use Policy, ale nie jest podstawowym obowiązkiem klasyfikacji „ryzyko ograniczone” w samym AI Act.

**P2 — dokumentacja i źródła:**  
Prowadzić dokumentację używanych modeli, źródeł danych, licencji, ograniczeń systemu i procesu aktualizacji danych. W dokumentacji wskazać, które informacje pochodzą z modeli AI, które z OSM/API/scrapingu, oraz jakie są znane ograniczenia jakości danych.

Źródła: oficjalny AI Act Service Desk / EUR-Lex dla [art. 50](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-50), [art. 53](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-53), [art. 54](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-54), [art. 55](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-55).

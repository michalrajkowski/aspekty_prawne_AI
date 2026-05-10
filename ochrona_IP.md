# Ochrona własności intelektualnej

## 1. Co chronimy

Rozdzielamy zasoby projektu na dwie warstwy, bo każda wymaga innego reżimu ochrony.

**Warstwa, którą chronimy aktywnie (nasz wkład twórczy):**
- **Kod aplikacji** — orkiestracja agentów, warstwa RAG, parsery, pipeline'y ETL danych turystycznych, integracje z API, frontend planera.
- **Architektura systemu wieloagentowego** — schemat przepływu między agentami, sposób dekompozycji zapytania użytkownika na podzapytania, strategia wyboru bazy wiedzy (POI vs. opisy semantyczne vs. dane czasu rzeczywistego z API).
- **Prompt engineering i konfiguracja agentów** — systemowe prompty, schematy narzędzi, logika fallbacków, reguły walidacji wejścia.
- **Know-how zespołu** — sposób strojenia retrievera dla danych geograficznych, heurystyki rankowania POI, doświadczenia z czyszczenia danych OSM/blogowych.
- **Dokumentacja techniczna i projektowa** w tym repo (README, AI_ACT, RODO, ewidencja zasobów, ten dokument).
- **Marka „Travel Planner”** (nazwa robocza) — gdyby projekt wszedł w fazę komercjalizacji.

**Warstwa, której NIE możemy objąć własną ochroną IP (cudze IP):**
- **Model Llama-PLLuM-70B-chat** — pozostaje własnością Meta/CYFRAGOVPL, używamy na warunkach Llama 3.1 Community License.
- **Dane OpenStreetMap** — własność społeczności OSM, ODbL 1.0; nasze pochodne bazy POI/embeddingi z OSM dziedziczą obowiązek share-alike (zgodnie z analizą w `licencje.md`).
- **Treści z Google Maps / TripAdvisor / blogów turystycznych** — używane w granicach ToS i dozwolonego użytku, nie są „naszą własnością intelektualną”, nawet po przetworzeniu przez RAG.
- **Biblioteki open source** (Playwright, Python, frameworki RAG) — pozostają na swoich licencjach.

## 2. Jak chronimy

### 2.1. Prawo autorskie

- **Kod i dokumentacja** powstają jako utwory w rozumieniu prawa autorskiego od momentu utrwalenia — ochrona przysługuje nam automatycznie, bez rejestracji.
- **Współautorstwo** — projekt tworzony przez 4-osobowy zespół; w razie komercjalizacji konieczne będzie uregulowanie udziałów (umowa między współtwórcami lub przeniesienie majątkowych praw autorskich na jeden podmiot, np. spółkę).
- **Praktyki techniczne wzmacniające ochronę:** historia commitów w Git jako dowód autorstwa i daty powstania, nagłówki copyright w plikach źródłowych, plik `LICENSE` w repo określający warunki dla osób trzecich, plik `NOTICE` zbierający wymagane atrybucje (Llama, OSM, Apache 2.0).

### 2.2. Własność przemysłowa

- **Patenty** — **nie planujemy.** System jest kompozycją znanych technik (RAG, agenci, retrieval geograficzny) bez przełomu technicznego, który spełniałby przesłankę nieoczywistości. Procedura patentowa (~5–10 lat, koszt rzędu kilkudziesięciu tysięcy złotych za zgłoszenie krajowe, znacznie więcej za EPO/PCT) jest niewspółmierna do skali projektu studenckiego.
- **Znaki towarowe** — **nie na obecnym etapie.** Nazwa „Travel Planner” jest opisowa i prawdopodobnie nie nadaje się do rejestracji jako znak słowny. Jeśli projekt wejdzie w komercjalizację, rozważymy rejestrację oryginalnej nazwy produktowej i logo w UPRP / EUIPO.
- **Wzory przemysłowe** — nie dotyczy (brak odróżniającego designu produktowego na obecnym etapie).

### 2.3. Tajemnica przedsiębiorstwa / know-how

Większość naszej realnej przewagi konkurencyjnej nie nadaje się do ochrony patentowej, ale nadaje się do ochrony jako tajemnica przedsiębiorstwa (art. 11 ustawy o zwalczaniu nieuczciwej konkurencji). Chronimy w tym trybie:

- finalne, dostrojone prompty systemowe agentów,
- konkretne wagi i parametry rankera POI,
- listy źródeł i konfiguracje scraperów (które serwisy, z jaką częstotliwością, z jakimi nagłówkami),
- wewnętrzne notatki o jakości danych z poszczególnych źródeł.

**Środki ochrony:** prywatne repozytorium dla wersji produkcyjnej (publiczne repo zawiera tylko warstwę dokumentacyjną i fragmenty kodu), kontrola dostępu, brak publikacji „pełnego stacku promptów” w pracach pisemnych ani materiałach demo.

### 2.4. Licencje — co wybieramy dla naszych własnych produktów

Projekt ma podwójny charakter: warstwa akademicka (dokumentacja, raporty, ten dokument) i warstwa techniczna (kod + ewentualny produkt). Stąd dwa różne wybory licencyjne.

- **Kod aplikacji — `Apache 2.0`.** Permisywna, kompatybilna z całym naszym stosem licencyjnym (MIT, BSD, PSFL, ODbL na warstwie danych, Llama Community License na warstwie modelu — analiza kompatybilności w `licencje.md`). Zawiera wyraźną klauzulę patentową (sekcja 3), co chroni nas i przyszłych użytkowników przed roszczeniami patentowymi. Pozwala na komercjalizację bez konieczności otwierania całego kodu, co nie byłoby możliwe pod GPL/AGPL.
- **Dokumentacja i raporty (to repo) — `CC BY 4.0`.** Pozwala na ponowne wykorzystanie z atrybucją, w tym przez innych studentów i badaczy.
- **Ewentualne pochodne bazy POI z OSM, jeśli zostaną opublikowane — `ODbL 1.0`** (wymuszone przez share-alike OSM, patrz `licencje.md`).
- **Dataset dialogów użytkowników** — **nie publikujemy** (kolizja z RODO, patrz pkt 3 poniżej).
- **Modele Llama-PLLuM** — nie redystrybuujemy; użytkownik końcowy pobiera je sam z Hugging Face, my dostarczamy wyłącznie integrację. To upraszcza obowiązki z Llama Community License.

## 3. Dlaczego — uzasadnienie strategii

### Dlaczego nie patentujemy

Patent wymaga nowości i nieoczywistości. Wieloagentowy RAG dla turystyki jest kompozycją znanych elementów; ryzyko unieważnienia w razie sporu byłoby wysokie, a koszt zgłoszenia i utrzymania nieproporcjonalny do potencjalnych przychodów na obecnym etapie. Lepiej tę samą wartość chronić jako know-how + szybkość iteracji.

### Dlaczego Apache 2.0, a nie GPL/AGPL ani licencja zamknięta

- **Nie GPL/AGPL** — copyleft odstraszyłby ewentualnego partnera komercyjnego (operatora hotelowego, miasto Wrocław, biuro turystyki) i zmusiłby go do otwierania własnych integracji.
- **Nie licencja w pełni zamknięta** — projekt powstaje w warstwie akademickiej, część kodu jest już publiczna; zamknięcie wszystkiego utrudniłoby publikacje i recenzję.
- **Apache 2.0 to złoty środek** — chroni nasze prawa autorskie i daje nam zabezpieczenie patentowe, jednocześnie nie blokuje przyszłej komercjalizacji.

### Czy możemy publikować dataset?

- **Dataset POI/embeddingi oparte na OSM** — *tak, ale tylko na ODbL* z udostępnieniem pliku zmian/metody przekształcenia (sekcja 4.6 ODbL).
- **Dataset zawierający scrapowane treści blogów lub recenzji TripAdvisor** — **nie.** Naruszałby to prawa autorskie autorów i ToS platform (zob. ewidencja zasobów). Możemy najwyżej publikować zagregowane statystyki nieumożliwiające rekonstrukcji oryginałów.
- **Dataset czysto syntetyczny** (przykładowe trasy, dialogi testowe) — *tak*, na CC BY 4.0.

### Czy możemy wysłać artykuł na konferencję?

**Tak — pod warunkami.** Artykuł może opisać architekturę, wyniki ewaluacji, wkład naukowy. Nie może zawierać pełnych promptów systemowych ani kompletnej konfiguracji scraperów (bo to nasze know-how i jego ujawnienie zniweczyłoby ochronę z art. 11 u.z.n.k.). Przed wysłaniem sprawdzamy politykę IP konferencji — niektóre wymagają licencji Creative Commons na pełny tekst, inne pozostawiają prawa autorom. Jeśli planowalibyśmy patent (czego nie planujemy), publikacja przed zgłoszeniem zniszczyłaby przesłankę nowości — to ostrzeżenie zostawiamy w dokumentacji na wypadek zmiany strategii.

### Czy możemy rozpocząć komercjalizację?

Z punktu widzenia naszego IP — tak. Apache 2.0 na nasz kod tego nie blokuje. **Realne ograniczenia leżą gdzie indziej** i muszą być zaadresowane przed wdrożeniem komercyjnym:

- **ToS Google Maps i TripAdvisor** — zakaz trwałego cachowania, limity wywołań, wymagana atrybucja, czasem zakaz konkurencyjnych zastosowań. Wymagałoby to renegocjacji warunków lub wymiany źródła danych.
- **ODbL** — przy publicznym wystawieniu produktu opartego o pochodną bazę POI musimy spełnić obowiązki share-alike i 4.6 ODbL.
- **Llama 3.1 Community License** — próg 700 mln MAU (nie grozi nam), obowiązek „Built with Llama”, zgodność z Acceptable Use Policy.
- **AI Act i RODO** — patrz `AI_ACT.md` i `RODO.md`.

### Co by się stało bez ochrony

- **Bez prawa autorskiego na kod** — każdy mógłby zabrać kod, sprzedać go pod własną marką, a my nie mielibyśmy podstawy do roszczeń. (W praktyce ochrona powstaje automatycznie, ale brak `LICENSE` w repo oznaczałby, że *nikt inny* nie może z kodu legalnie korzystać — co paradoksalnie utrudniłoby też naszą własną dystrybucję i adopcję.)
- **Bez know-how chronionego jako tajemnica** — opublikowanie pełnych promptów i konfiguracji scraperów oznacza, że konkurent w godzinę odtwarza naszą jakość wyników bez ponoszenia kosztu iteracji.
- **Bez świadomej polityki licencyjnej zasobów wejściowych** (OSM, Llama, blogi) — ryzyko roszczeń od OSMF, Meta, autorów blogów lub operatorów platform. W skrajnym przypadku konieczność wycofania systemu z użycia.
- **Bez separacji warstw** (nasz kod ↔ dane OSM ↔ model Llama) — zarażenie warunkami ODbL/Llama elementów, które powinny zostać pod naszą kontrolą.

**Werdykt operacyjny strategii IP:** chronimy *autorski wkład* (kod + know-how) możliwie najtaniej i najprościej (prawo autorskie + Apache 2.0 + tajemnica przedsiębiorstwa); świadomie *nie próbujemy* obejmować ochroną IP cudzych zasobów (OSM, Llama, blogi); wszystkie obowiązki licencyjne wynikające z zasobów zewnętrznych traktujemy nie jako naszą ochronę IP, ale jako *zobowiązania do spełnienia*, opisane w `licencje.md` i `ewidencja_zasobow_i_licencje.md`.

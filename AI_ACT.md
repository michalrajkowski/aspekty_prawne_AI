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
Najbardziej właściwą klasyfikacją dla całego systemu jest ryzyko ograniczone. Travel Planner działa jako chatbot/asystent AI, który rozmawia z użytkownikiem w języku naturalnym, interpretuje jego preferencje i generuje propozycje planów wycieczek. Z tego powodu użytkownik powinien być jasno poinformowany, że rozmawia z systemem AI, a wygenerowany plan jest rekomendacją, nie gwarancją poprawności ani aktualności danych. System powinien także komunikować ograniczenia dotyczące cen, godzin otwarcia, dostępności atrakcji, remontów, warunków pogodowych i jakości danych źródłowych.

## Dodatkowe wymagania: transparentność i GPAI

Tak, nasz system podlega dodatkowym wymaganiom transparentności, ponieważ działa jako chatbot/asystent AI i generuje treści dla użytkownika. Użytkownik powinien być jasno poinformowany, że rozmawia z systemem AI, a wygenerowane plany wycieczek, opisy tras i rekomendacje są treściami wygenerowanymi automatycznie.

System powinien także oznaczać lub opisywać ograniczenia wygenerowanych treści, zwłaszcza że mogą one dotyczyć zmiennych informacji: cen, godzin otwarcia, dostępności atrakcji, remontów, komunikacji miejskiej, pogody czy bezpieczeństwa trasy. Rekomendacje nie powinny być przedstawiane jako pewne lub oficjalne informacje, jeśli pochodzą z modelu albo z danych, które mogą być nieaktualne.

W zakresie GPAI główne obowiązki dotyczą przede wszystkim dostawców modeli ogólnego przeznaczenia, np. dostawców API LLM albo twórców modeli open-weight. Jako twórcy aplikacji korzystającej z takich modeli powinniśmy jednak dokumentować, z jakich modeli korzystamy, wybierać dostawców zgodnych z AI Act, przestrzegać ich warunków użycia oraz wdrożyć zabezpieczenia po stronie aplikacji, np. filtrowanie niebezpiecznych zapytań, ograniczanie halucynacji i informowanie użytkownika o źródłach danych.


## Dodatkowe wymagania i zmiany potrzebne do zgodności z AI Act

Nasz system podlega dodatkowym wymaganiom transparentności, ponieważ działa jako chatbot/asystent AI i generuje treści dla użytkownika. Użytkownik powinien być jasno poinformowany, że rozmawia z systemem AI, a plany wycieczek, opisy tras i rekomendacje są generowane automatycznie. System powinien też komunikować ograniczenia odpowiedzi, szczególnie w zakresie aktualności cen, godzin otwarcia, dostępności atrakcji, remontów, pogody i bezpieczeństwa tras.

W zakresie GPAI główne obowiązki dotyczą przede wszystkim dostawców modeli ogólnego przeznaczenia, np. OpenAI albo twórców modeli open-weight. Jako twórcy aplikacji korzystającej z takich modeli powinniśmy jednak dokumentować, z jakich modeli korzystamy, wybierać dostawców zgodnych z AI Act oraz przestrzegać ich warunków użycia.

Żeby spełnić wymagania AI Act, musielibyśmy dodać w projekcie jasny komunikat, że użytkownik korzysta z AI, oraz oznaczać wygenerowane plany jako rekomendacje, a nie oficjalne lub gwarantowane informacje. Należałoby też prowadzić dokumentację używanych modeli, źródeł danych i ograniczeń systemu, wdrożyć podstawowe mechanizmy bezpieczeństwa, np. filtrowanie niebezpiecznych zapytań, oraz zapewnić możliwość zgłaszania błędnych lub ryzykownych rekomendacji.

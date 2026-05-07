Aspekty etyczne (15 pkt)
Jedna spójna sekcja obejmująca cztery wymiary etyczne Waszego projektu:

- Przejrzystość — gdzie i do czego korzystacie z AI? Co jest automatyczne, a gdzie jest człowiek w pętli? Co udostępniacie (kod, dane, wyniki)?
- Wyjaśnialność — jakie problemy etyczne mogą się pojawić (dyskryminacja, prywatność, niesprawiedliwe decyzje)? Jak im zapobiegacie?
- Inkluzywność — wpływ na rynek pracy, potencjalna dyskryminacja, jakość i pokrycie danych.
- Wyrównanie (alignment) — zgodność z ramami prawnymi (RODO, AI Act, prawo autorskie, regulacje branżowe).

---

## Przejrzystość
- **Wykorzystanie AI:** Sztuczna inteligencja jest wykorzystywana do przetwarzania języka naturalnego (rozmowy z klientem poprzez wykorzystany mdoel językowy).
Automatycznie odbywa się wyszukiwanie wektorowe (RAG) i zapytania do API (OSM) oraz ukłądanie lanu wycieczki
- **Człowiek w pętli:** System ma charakter doradczy, co oznacza, że ostetczną decyzję odnośie planu oraz elementów wycieczki dokonuje użytkownik, który może narzucic swoje wybory systemowi. Wszelkich rezerwacji biletów itp. użytkonik musi tez sam dokonać.
- **Udostępnianie:** Dla potencjalnych klientów udostepniamy zarówno kod jak i bazę wiedzy (zbiór danych). Natomiast użytkownik końcowy korzysta wyłącznie z interfejsu systemu i nie ma wglądu ani w kod, ani bezpośrednio w zbiór danych.

## Wyjasnialność
**Zidentyfikowane ryzyka:** 
- Halucynacje modeli językowych, przez co mogłyby polecić nieistniejące już restauracje, czy niezaktualizowane godiny otwarcia atrakcji. Z tego względu zdecydowalismy się na wykorzystanie systemu RAG, w którym LLM korzysta z bazy wiedzy, która jest na bieżąco aktualizowana o najnowsze informacje. Dodatkowo model językowy po zaproponowaniu jakiejs atrakcji poweinien powołać się na nią i podac np. link do jej oficjalnej strony, tak aby użytkownik mógł sprawdzić aktualność danych z oficjalnymi źródłami. 

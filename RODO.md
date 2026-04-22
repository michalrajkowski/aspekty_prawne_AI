RODO (15 pkt)

- Czy przetwarzacie dane osobowe? Jeśli tak — podajcie przykłady i dlaczego uznajecie je za dane osobowe. Jeśli nie — uzasadnijcie i opiszcie hipotetyczny scenariusz, w którym moglibyście je przetwarzać.
- Cele i podstawy prawne przetwarzania.
- Kto, kiedy i w jaki sposób ma dostęp do danych?
- Obowiązki wynikające z RODO — co musicie zapewnić?
- Sankcje i ryzyka — co grozi za naruszenia?

---

## 1. Gdzie mogą u nas pojawić się dane osobowe + dlaczego są to dane osobowe?

Nasz system może przetwarzać dane osobowe. Część z nich jest niepożądanym zjawiskiem wynikającym ze źródeł danych, które wykorzystujemy w systemie. Inne są czymś wymaganym od samego początku.

Zgodnie z definicją RODO, danymi osobowymi są wszelkie informacje o zidentyfikowanej lub możliwej do zidentyfikowania osobie fizycznej.

### a) Dane osobowe "przypadkowe"

- Dane będące artefaktami scrapowania zawartości Google i stron internetowych:
  - Pobieramy zawartość stron internetowych powiązanych z atrakcjami:
    - Strony internetowe mogą zawierać dane osobowe, numery telefonu, adresy e-mail itp.
  - Pobieramy komentarze z Google Maps:
    - Mogą zawierać imię, nazwisko oraz zdjęcie profilowe (np. twarz użytkownika)
    - Dodatkowo komentarz może zawierać dane osobowe w treści, co jest trudniejsze do anonimizacji

- Wiadomości wymieniane między użytkownikiem a systemem:
  - Użytkownik może podać dane osobowe wewnątrz swoich promptów
  - W trakcie rozmowy system rozbudowuje zbiór jego pozytywnych i negatywnych preferencji

### b) Dane osobowe "zaplanowane"

- Dane annotatorów:
  - Nasz system będzie ewaluowany z pomocą annotatorów
  - Ze względów logistycznych konieczne będzie powiązanie wyników pracy annotatora z dostarczonymi plikami
  - W związku z tym na pewnym etapie pojawiają się jego dane osobowe

- Adresy IP / fingerprint:
  - Jeżeli system będzie udostępniany jako usługa, konieczne może być blokowanie użytkowników działających szkodliwie
  - W tym celu należy prowadzić rejestr adresów IP / fingerprintów użytkowników:
    - tych, którzy korzystali z usługi
    - oraz tych, których chcemy zablokować
   
## 2. Cele i podstawy prawne przetwarzania

* **Pobieranie opinii z Google Maps i stron (Dane przypadkowe):** Celem jest budowa wektorowej bazy wiedzy dla systemu RAG, aby asystent mógł udzielać merytorycznych i poprawnych odpowiedzi. Podstawą prawną jest prawnie uzasadniony interes administratora (Art. 6 ust. 1 lit. f RODO). Budujemy innowacyjną usługę wyszukiwania, stosując przy tym zasadę minimalizacji danych.
* **Przetwarzanie logów / adresów IP użytkowników:** Cel to zapewnienie cyberbezpieczeństwa systemu, zapobieganie atakom (np. DDoS) oraz limitowanie zapytań. Podstawą prawną jest prawnie uzasadniony interes administratora (Art. 6 ust. 1 lit. f RODO) w zakresie bezpieczeństwa sieci i informacji.
* **Przetwarzanie promptów użytkownika (konwersacja z asystentem):** Celem jest świadczenie usługi asystenta AI oraz personalizacja wyników w trakcie sesji. Podstawą prawną jest niezbędność do wykonania umowy (Art. 6 ust. 1 lit. b RODO), ponieważ świadczymy usługę zgodnie z zaakceptowanym przez użytkownika regulaminem.
* **Dane annotatorów:** Celem jest ewaluacja modelu, komunikacja projektowa oraz rozliczenia. Podstawą prawną jest niezbędność do wykonania umowy (Art. 6 ust. 1 lit. b RODO).

## 3. Kto, kiedy i w jaki sposób ma dostęp do danych?

**Kto ma dostęp:**
* **Zespół PNW:** Nasz zespół ma pełen dostęp administracyjny do baz danych, logów i surowych plików źródłowych.
* **Zewnętrzni dostawcy:** Dostawcy modeli AI lub infrastruktury chmurowej - umowy powierzenia przetwarzania danych (DPA).

**Kiedy następuje dostęp:**
Podczas fazy developmentu systemu, scrapowania, utrzymania systemu (debugging) oraz analizy logów bezpieczeństwa.

**W jaki sposób realizowany jest dostęp:**

## 4. Obowiązki wynikające z RODO — co musicie zapewnić?

Jako administratorzy danych musimy architektonicznie i prawnie wdrożyć poniższe zasady.

* **Zasada minimalizacji danych i Privacy by Design:** W etapie potoku danych powinnismy wdrozyć filtry usuwające dane osobowe (np. nazwiska, zdjęcia) ze scrapowanych recenzji, zanim trafią one do bazy wektorowej.
* **Obowiązek informacyjny (Art. 13 i 14 RODO):** Musimy przygotować jasną Politykę Prywatności, w której wytłumaczone będzie jak długo przechowujemy zapis  rozmów oraz adresy IP uzytkowników, a także jakim firmom zewnętrznym je przekazujemy.
* **Prawa osób, których dane dotyczą:** Należy zapewnić użytkownikom możliwość usunięcia ich historii czatu lub wglądu w przetwarzane dane.

## 5. Sankcje i ryzyka — co grozi za naruszenia?

Niestosowanie się do przepisów RODO niesie za sobą poważne konsekwencje na wielu płaszczyznach.

* **Kary administracyjne (finansowe):** Wymierzane przez Prezesa UODO. Za lżejsze naruszenia kara sięga do 10 mln EUR lub 2% całkowitego rocznego światowego obrotu. Za najcięższe przewinienia (np. rażące naruszenie podstawowych praw, ignorowanie żądań usunięcia danych) grozi do 20 mln EUR lub 4% obrotu.
* **Działania naprawcze UODO:** Urząd może nakazać tymczasowe lub całkowite ograniczenie przetwarzania. W praktyce oznacza to nakaz wyłączenia systemu i całkowitego usunięcia nielegalnie zbudowanej bazy wektorowej.
* **Odpowiedzialność cywilna:** Osoby, których dane wyciekły z systemu, mogą domagać się przed sądem odszkodowania za poniesione szkody.
* **Ryzyko wizerunkowe:** Utrata zaufania użytkowników do naszego systemu. 

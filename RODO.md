RODO (15 pkt)

- Czy przetwarzacie dane osobowe? Jeśli tak — podajcie przykłady i dlaczego uznajecie je za dane osobowe. Jeśli nie — uzasadnijcie i opiszcie hipotetyczny scenariusz, w którym moglibyście je przetwarzać.
- Cele i podstawy prawne przetwarzania.
- Kto, kiedy i w jaki sposób ma dostęp do danych?
- Obowiązki wynikające z RODO — co musicie zapewnić?
- Sankcje i ryzyka — co grozi za naruszenia?

---

## 1. Gdzie mogą u nas pojawić się dane osobowe + dlaczego są to dane osobowe?

Nasz system może przetwarzać dane osobowe. Część z nich jest niepożądanym zjawiskiem wynikającym ze źródeł danych, które wykorzystujemy w systemie. Inne są czymś wymaganym od samego początku.

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
   
  

| Sekcja | Opis |
|---|---|
| Tytuł projektu | Travel Planer |
| Lista osób zaangażowanych | Michał Rajkowski (248821)<br>Michał Bernacki-Janson (**indeks**)<br>Mateusz Zbrocki (**indeks**)<br>Julianna Godziszewska (263841) |
| One-liner — cel projektu | Stworzenie planera wycieczek AI |
| Krótki opis (max ½ A4) | Rozbudowany wieloagentowy RAG, który potrafi zaplanować wycieczkę z użytkownikiem (na bazie rozmowy w języku naturalnym) i wykorzystać do tego zarówno dane przestrzenne (punkty zainteresowań na mapie, trasy) jak i ceny, cechy atrakcji. <br><br> Dodatkowo asystent uwzględnia w zwróconych trasach preferencje semantyczne użytkownika. <br><br> System wykorzystuje wiele baz wiedzy odnośnie punktów turystycznychi wrocławia, dane OSM, opisy stron internetowych powiązane z atrakcjami, jak i posiada dostęp do API w celu weryfikacji aktualnych danych.|
| Grafika (opcjonalna) | TODO: Diagram ilustrujący projekt, flow przetwarzania, zrzut ekranu z dema |
| Problemy IP | TODO: Jakie problemy związane z własnością intelektualną zauważacie już w projekcie? Każda osoba wpisuje jedną: 1. @imie.nazwisko ... <br> 1. @Michał.Rajkowski : Scrapowanie stron internetowych / wyłuskiwanie informacji ze stron do naszej bazy wiedzy.<br> 2. @Julianna.Godziszewska : Naruszenie polityki użycia API -Niedozwolone i trwałe buforowanie danych w bazie wiedzy (np. TripAdvisor) lub obowiązek ich cyklicznego usuwania i odświeżania (np. max 30 dni w przypadku GoogleMaps). <br> 3. <br> 4.|
| Wyzwania etyczne/społeczne | - w przypadku rozbudowania profilu użytkownika, RODO, bo zbieramy dane personalne i "profilujemy" osobę, która będzie korzystała z systemu <br>    - RODO dotyczy nas nawet gdy nie będziemy budować profili tylko po prostu zapisywać historię konwersacji co jest bardzo prawdopodobne (bo nie wiadomo czy ktoś nie podał sam swoich danych albo jakiś krytycznych informacji w rozmowie z czatem) <br> - system musi odmawiać użytkownikom odpowiedzi na "nielegalne" pytania lub kierować rozmowę na inne tory |

---

<h1 style="display: flex; align-items: center; gap: 8px;">
  <span>Prompty do Chatów</span>
  <img
    src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/ChatGPT_logo.svg/960px-ChatGPT_logo.svg.png"
    alt="ChatGPT logo"
    width="32"
  />
</h1>

> "(przeklejenie całej tabelki z opisami) Jakie mogą być ogólne problemy z własnością intelektualną w projektach tego typu?"

> "Podaj mi przykłady API (które mozemy wykorzystać w naszym projekcie), które mają rygorystyczne zasady dotyczące cachowania danych."

> "Opowiedz mi o "wyzwaniach etycznych" (AI Act, dane osobowe, generowanie treści, itp.) które mogą być związane z realizacją projektu opartego o budowę RAG do planowania miejskich wycieczek. Tematyka projektu zahacza o zbieranie danych atrakcji turystycznych, hoteli, restauracji, wykorzystywanie danych z GoogleMaps i OSM, budowanie baz wiedzy, zapytania do API, przetwarzanie wiadomości użytkownika itp"

> "a co z informacjami gdy użytkownik poda coś nielegalnego lub będzie pytał o nielegalne rzeczy?"

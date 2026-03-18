# Ewidencja zasobow i licencje

## Ewidencja (15 pkt)

Przygotujcie szczegolowa ewidencje wszystkich zasobow wykorzystywanych i tworzonych w projekcie:
- zbiory danych (gotowe i tworzone przez Was),
- modele ML (pobierane z HuggingFace, API LLM-ow, itp.),
- repozytoria kodu (wlasne i cudze),
- Wasze docelowo wytrenowane modele.

| ID | Nazwa zasobu | Typ zasobu | Opis | Lokalizacja / URL | Licencja | Link do licencji | @kto |
|---|---|---|---|---|---|---|---|
| 1 | OpenStreetMap | Zbior danych / dane mapowe | Otwarte dane mapowe wykorzystywane do punktow POI, geometrii i sieci drogowej/pieszej. | https://www.openstreetmap.org | ODbL 1.0 | https://opendatacommons.org/licenses/odbl/1-0/ | @mateusz.zbrocki |
| 2 | Nominatim (publiczne API) | API / geokodowanie | Wyszukiwanie miejsc i reverse geocoding na danych OSM; obowiazuja limity i warunki publicznej instancji. | https://nominatim.openstreetmap.org | OSMF Nominatim Usage Policy | https://operations.osmfoundation.org/policies/nominatim/ | @mateusz.zbrocki |
| 3 | R5 (Conveyal) | Silnik routingu / transport | Analizy transportowe i liczenie czasow dojazdu dla ruchu pieszego, rowerowego, samochodowego i transportu publicznego. | https://github.com/conveyal/r5 | MIT | https://github.com/conveyal/r5/blob/dev/LICENSE | @mateusz.zbrocki |
| 4 | NetworkX | Biblioteka Python | Reprezentacja grafow i algorytmy grafowe do pracy na sieci polaczen, tras i zaleznosci miedzy punktami. | https://networkx.org | BSD 3-Clause | https://networkx.org/documentation/stable/ | @mateusz.zbrocki |
| 5 | r5py | Biblioteka Python | Pythonowy wrapper do R5, uzywany do wyznaczania tras, macierzy czasow przejazdu i analiz dostepnosci transportowej. | https://r5py.readthedocs.io/stable/ | GPL-3.0-or-later OR MIT | https://r5py.readthedocs.io/stable/user-guide/citation.html | @mateusz.zbrocki |
| 6 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 7 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 8 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 9 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 10 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 11 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 12 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 13 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 14 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 15 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 16 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |

---

Uwagi robocze:
- Wpis dla Nominatim zaklada korzystanie z publicznego API OSMF.
- `R5` i `r5py` sa wpisane osobno: silnik Java i wrapper Python to dwa rozne zasoby.

<h1 style="display: flex; align-items: center; gap: 8px;">
  <span>Prompty do Chatów</span>
  <img
    src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/04/ChatGPT_logo.svg/960px-ChatGPT_logo.svg.png"
    alt="ChatGPT logo"
    width="32"
  />
</h1>

> Ok, chciabym zacząć uzupełniać tablekę.
> Na pewno używamy
> 1. open street map
> 2. nominatim
> 3. r5 (for transport)
> 4. networkx
> 
> all in python

> ": )"

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
| 6 | LangChain | Biblioteka Python | Framework do budowania agentów i aplikacji opartych na LLM. Umożliwia łączenie interoperacyjnych komponentów i integracji zewnętrznych, upraszczając tworzenie aplikacji A| https://github.com/langchain-ai/langchain | MIT | https://github.com/langchain-ai/langchain/blob/master/LICENSE | @Julianna.Godziszewska |
| 7 | LangGraph | Biblioteka Python | Niskopoziomowy framework orkiestracyjny przeznaczony do budowy agentów stanowych (stateful agents). | https://github.com/langchain-ai/langgraph | MIT | https://github.com/langchain-ai/langgraph/blob/main/LICENSE | @Julianna.Godziszewska |
| 8 | OpenAI (modele GPT) | API / Model ML | Główny model językowy sterujący logiką agentów, generujący plany wycieczek na podstawie danych przestrzennych i tekstowych. | https://platform.openai.com | Komercyjna (API ToS) | https://openai.com/policies/terms-of-use/ | @Julianna.Godziszewska |
| 9 | Playwright | Biblioteka Python | Główny framework do automatyzacji przeglądarki, służący do obsługi dynamicznych elementów i scrapowania danych z witryn internetowych. | https://playwright.dev/python/ | Apache 2.0 | https://github.com/microsoft/playwright-python/blob/main/LICENSE | @Julianna.Godziszewska |
| 10 | BAAI/BGE-M3 | embedding model | Bardzo dobry model do tworzenia osadzeń tekstowych, co ciekawe jednocześnie Chiński i na licencji MIT | [Huggingface](https://huggingface.co/BAAI/bge-m3), [repozytorium git](https://github.com/FlagOpen/FlagEmbedding/blob/master/LICENSE) | MIT |  [repozytorium git](https://github.com/FlagOpen/FlagEmbedding/blob/master/LICENSE) | @michal.rajkowski |
| 11 | DeepSeek-R1 | reasoningowy llm | Bardzo dobry LLM z reasoningiem. Co ciekawe ma wiele wersji i niektóre są na innej licencji [1] | [Huggingface](https://huggingface.co/deepseek-ai/DeepSeek-R1) | MIT[1] | [Huggingface](https://huggingface.co/deepseek-ai/DeepSeek-R1/blob/main/LICENSE) , [dodatkowy dopisek](https://huggingface.co/deepseek-ai/DeepSeek-R1#7-license) | @michal.rajkowski |
| 12 | openai/gpt-oss-120 | Otwartowagowy LLM | Bardzo dobry model LLM otwartowagowy. | [Huggingface](https://huggingface.co/openai/gpt-oss-120b), [Karta modeli](https://openai.com/index/gpt-oss-model-card/) | Apache 2.0 + Usage Policy [2] | [Huggingface](https://huggingface.co/openai/gpt-oss-120b/blob/main/LICENSE) | @michal.rajkowski |
| 13 | CYFRAGOVPL/Llama-PLLuM-70B-chat | polski LLM  | Poslki LLM wytworzony przy współpracy z Politechniką Wrocławską | [Huggingface](https://huggingface.co/CYFRAGOVPL/Llama-PLLuM-70B-chat) | Llama 3.1 | [Huggingface](https://huggingface.co/CYFRAGOVPL/Llama-PLLuM-70B-chat/blob/main/LICENSE) | @michal.rajkowski |
| 14 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 15 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |
| 16 | TODO | TODO | TODO | TODO | TODO | TODO | @imie.nazwisko |

[1] - co ciekawe niektóre wersje DeepSeek'a-R1 posiadają inną licencję niż MIT, bo np. były bazowane na Qwen'ach podlegających pod licencję Apache 2.0, albo Llamach: https://huggingface.co/deepseek-ai/DeepSeek-R1#7-license.

[2] - obok licencji jest także zawarty [USAGE_POLICY](https://huggingface.co/openai/gpt-oss-120b/blob/main/USAGE_POLICY). 

---
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

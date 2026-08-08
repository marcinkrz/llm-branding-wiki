---
typ: playbook
etap: 04
nazwa: Konkurencja
aktualizacja: 2026-08-07
---

# 04 Konkurencja

## Cel
Poznać, **o kogo i o co** konkurujemy — nie wg firmy, lecz wg perspektywy klienta (którą alternatywę rozważa klient, gdy nie kupuje nas). To podstawa pozycjonowania.

## Decyzje (które tu zapadają)
- Kim są prawdziwi rywale (vs. kto jest „konkurencją" tylko na papierze).
- Na jakiej płaszczyźnie konkurujemy (cena, wygoda, jakość, marka).
- Gdzie jest przestrzeń do wyróżnienia (luka).

## Dane wejściowe
- Dane z researchu ([[Playbooki/02 Research|02]]), dane o kliencie (kogo rozważa).
- Lista firm z briefu + firmy z recenzji/wywiadów klientów.

## Kroki
1. **Zbierz listę kandydatów** na konkurencję: z briefu, researchu, wywiadów klientów.
2. **Ustal prawdziwych rywali vs. zamienniki** (w tym „zrób to sam", obróbka, inna kategoria) — z perspektywy klienta (JTBD).
3. **Sporządź profil każdego rywala**:
   - co komunikują (przekaz, obietnica),
   - ceny / model,
   - mocne i słabe strony (naczej z recenzji niż z ich deklaracji),
   - wyróżniki (czym się chwalą).
4. **Zbuduj mapę konkurencji** (wymiar decydujący dla klienta × drugi wymiar).
5. **Znajdź luki**: co klient kwestionuje w ofertach rywali (recenzje, wywiady).
6. **Oceń**, czy luka jest realna (klienci by nią pogardzili?) — nie tylko „nikt tego nie robi".

### Research konkurencji przez agenta (LLM + Internet)

> Agent może i powinien wykonać **większość researchu konkurencji sam**, wyszukując publicznych informacji w Internecie (to dane otwarte: strony, cenniki, komunikaty, recenzje, social). Klient dodaje **swoje przykłady** konkurencji (które zna z rynku/terenu) — lista z Internetu + lista od klienta łączą się.

1. **Agent wyszukuje**: strony konkurentów, cenniki, opisy usług, media społecznościowe, recenzje (Google Maps, Ceneo/Opineo, opinie), wzmianki, pozycje w wyszukiwarce, reklamy.
2. **Klient dodaje**: kogo sam zna, kogo „widzi na co dzień", kto mu zabiera zlecenia, kogo klienci wymieniają jako alternatywę (to dane, których nie znajdziesz w Google).
3. **Krzyżuj dane**: lista agenta (szersza, zewnętrzna) + lista klienta (bliższa, terenowa) → razem dają pełny obraz.
4. **Zaznacz źródła**: co pochodzi z wyszukiwania, co od klienta (różne pewność).
5. **Uwaga na „dane, których nie widać"**: klient zna zamienniki i status quo lepiej niż agent — jego input nie jest opcjonalny, tylko uzupełniający.

**Zrzuty ekranu konkurencji (do porównania wizualnego):**

Dla każdego kluczowego rywala agent robi **zrzut strony głównej** i zapisuje w folderze projektu `Badanie/konkurencja/` jako plik PNG (nazwa: `numer-Nazwa-rywala.png`). Obok w `porownanie-wizualne.md` notuje: URL, datę, look&feel (kolory, ton, układ, navi), wrażenie. Cel: **materiał referencyjny** do porównania przy pozycjonowaniu (czy się wizualnie odróżniamy — [[Frameworki/49 Mapa percepcyjna|mapa]], [[Frameworki/38 Kolor w brandingu|distinctive assets]]) oraz do dyskusji z klientem (konkret, nie ogólnie).

- Zrzut to **dane wewnętrzne analizy** (nie do powielania/reklamy) — oznacz folder jako „do analizy".
- Jeśli zrzut strony się nie powiedzie (loginy, dynamiczne treści, blokada) — zapisz opis wyglądu/key elementów i zanotuj „zrzut niemożliwy, zapisano opis".

**Podział pracy:** agent = wykrywanie, porządkowanie, profilowanie, zrzuty (skala). Klient = walidacja, kontekst, „kogo faktycznie przegrywam". Nie zastępuj klienta — pytaj go lista od początku ([[Prompty/Etap 04 Konkurencja|prompt 04]] prowadzi to automatycznie).

## Narzędzia (frameworki)
- [[Frameworki/05 Market Positioning Canvas|Market Positioning Canvas]] — dobór rywali + przewaga.
- [[Frameworki/04 Pozycjonowanie Ries Trout|Ries & Trout]] — kategoryzacja umysłu klienta.
- [[Frameworki/07 Blue Ocean Strategy|Blue Ocean]] — gdy rozważasz nową kategorię.
- [[Frameworki/02 Jobs To Be Done|JTBD]] — właściwi rywale wg jobów.

## Artefakt wynikowy
- **Mapa konkurencji** (kto, co, jak się pozycjonuje).
- **Lista prawdziwych rywali** (klient-perspektywa).
- **Zidentyfikowane luki** do rozważenia w pozycjonowaniu.

## Walidacja
- Lista rywali oparta na danych (co klient rozważa), nie na deklaracji firmy.
- Profil każdego rywala ma źródła (strony, recenzje, wywiady).
- Luki są opisane od strony klienta („klienci narzekają, że…").
- Ocena: czy nasza forma przewagi daje się obronić.

## Najczęstsze błędy
- Analiza konkurencji z biurka (same strony bez perspektywy klienta).
- Ignorowanie zamienników („robimy to inaczej" bez zrozumienia).
- Umieszczanie się na mapie „obok" bez decyzji o przewadze.
- „Nikt tego nie robi" = luka (to często znak, że nikt tego nie chce).

## Przekazanie dalej
→ [[Playbooki/05 Rynek|05 Rynek]] (warunki rynkowe), → [[Playbooki/06 Pozycjonowanie|06 Pozycjonowanie]] (decyzja o miejscu).

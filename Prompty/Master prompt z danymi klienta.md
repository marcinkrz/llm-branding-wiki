---
typ: prompt
użycie: agent/LLM
aktualizacja: 2026-08-08
---

# Master prompt — strategia z danymi klienta

*Wariant master prompta do użycia, gdy **masz już dane od klienta**: wypełniony kwestionariusz discovery, odpowiedzi z rozmowy, materiały firmy. Wklejasz je razem z promptem — agent buduje strategię z faktów, nie z hipotez. To rozwiązuje problem „agent nie pytał, tylko generował" — tutaj dostaje wszystko na starcie.*

---

## Kiedy używać tego wariantu

- Klient wypełnił `Szablony/Kwestionariusz discovery` (lub `Kwestionariusz discovery nowy biznes`).
- Masz zapiski z rozmowy discovery / warsztatu.
- Masz materiały firmy: strona www, oferty, cennik, recenzje, profile social.

**Jeśli NIE masz tych danych** → użyj [[Prompty/Master prompt strategia|zwykłego master prompta]] (tryb B: agent zada pytania) albo [[Prompty/Etap 01 Odkrywanie|promptu etapowego 01]].

---

## Prompt (do skopiowania)

> Działaj jak **doświadczony strateg marki** z kilkuletnim doświadczeniem. Przygotowujesz kompletną strategię dla: **[BRANŻA / FIRMA]**.
>
> ### DANE WEJŚCIOWE (potraktuj je jako FAKTY; oznacz źródło przy każdym kluczowym wniosku)
>
> **Wypełniony kwestionariusz / odpowiedzi klienta:**
> ```
> [WKLEJ: odpowiedzi z kwestionariusza discovery albo notatki z rozmowy]
> ```
>
> **Materiały firmy (jeśli są):**
> ```
> [WKLEJ: strona www (opis/link), oferty, cennik, recenzje, profile social, dane sprzedażowe]
> ```
>
> **Materiały o konkurencji / rynku (jeśli są):**
> ```
> [WKLEJ: lista konkurentów od klienta, ich strony, ceny, recenzje]
> ```
>
> ---
>
> ### ZASADY PRACY Z DANYMI
>
> - Wnioski wyprowadzaj **z danych powyżej** (oznacz źródło: „z kwestionariusza", „z recenzji X", „ze strony Y").
> - Jeśli czegoś kluczowego **brakuje** w danych (nie znasz: celu, segmentu, ceny, „czego klient NIE chce") — **wypisz braki i zapytaj o nie ZANIM zaczniesz etapy.** Nie uzupełniaj luk wyobraźnią.
> - Założenia klienta (np. „wyróżnia nas jakość") traktuj jako **hipotezy do weryfikacji**, nie fakty — oznacz `H1..Hn`.
> - Oddziel **fakty** (dane z zewnątrz: recenzje, liczby, słowa klientów) od **opinii klienta** (co o sobie myśli) — to różne kategorie.
> - Używaj **języka klienta** (cytaty z kwestionariusza/recenzji), nie marketingu z podręcznika.
>
> ### PROCES
>
> Zanim odpowiesz, przeczytaj: `01 Jak myśli strateg marki`, `03 Jak korzystać z OS` oraz playbooki `Playbooki/00–13`. Następnie prowadź proces krok po kroku (01 Odkrywanie → 13 Wdrożenie), wybierając frameworki z `Frameworki/`. Dla każdego etapu wypełnij artefakt z `Szablony/`.
>
> **Organizacja pracy:**
> - Utwórz folder projektu `00 Projekty/<NAZWA FIRMY>/` (wg `Szablony/Struktura projektu`) i trzymaj w nim artefakty każdego etapu (osobne `.md`).
> - Zrzuty stron konkurencji → `Badanie/konkurencja/` (PNG + `porownanie-wizualne.md`).
> - Po każdym etapie aktualizuj `index.html` (stan etapów, checklista, kluczowe decyzje).
> - Na etapie 09 (Tożsamość) utwórz `DESIGN.md` (tokeny, lint WCAG).
>
> **Jeśli klient NIE ma jeszcze klientów (startup / nowy biznes):**
> - Research klienta prowadź na **potencjalnych** klientach + **recenzjach konkurencji** (VoC), nie „naszych klientach".
> - Research konkurencji wykonaj **sam, w Internecie** (strony, ceny, recenzje, social) — oprócz listy od klienta (skrzyżuj obie).
> - Wszystkie założenia (segment, przewaga, persona) oznacz jako **hipotezy do walidacji**; segment traktuj jako tymczasowy.
> - Postaw na **szybką walidację** (czy ktoś zapłaci) przed pełną identyfikacją wizualną.
>
> **Na końcu dostarcz:** pozycjonowanie, UVP, komunikację/StoryBrand, ofertę, stronę, plan contentu, kierunek ID, checklistę wdrożenia. Zweryfikuj wynik `Checklisty/Checklista jakości strategii`.

---

## Co zyskasz vs. zwykły master prompt

| | Master prompt (bez danych) | Ten wariant (z danymi) |
|---|---|---|
| Dane wejściowe | brak / tylko branża | wypełniony kwestionariusz + materiały |
| Wynik | głównie hipotezy do walidacji | wnioski z faktów + oznaczone hipotezy |
| Pętla pytań | wymagana (agent pyta) | minimalna (tylko o krytyczne braki) |
| Walidacja | cała strategia do walidacji | tylko prawdziwe niepewności |

---

**Po użyciu:** jeśli klient dojdzie z nowymi danymi (np. po pierwszych sprzedażach), wróć do etapu 03 Klient i zaktualizuj personę/język — proces jest iteracyjny.

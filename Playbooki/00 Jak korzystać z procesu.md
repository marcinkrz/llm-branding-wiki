---
typ: playbook-intro
aktualizacja: 2026-08-07
---

# Jak korzystać z procesu (playbooki)

*Playbooki to **procedury** — odpowiedź na pytanie „jak to zrobić krok po kroku?". Oddzielone od wiedzy ([[Wiedza/Wiedza|Wiedza]]) i narzędzi ([[Frameworki/Frameworki|Frameworki]]) zgodnie z Zasadą 4 ([[02 Zasady]]).*

## O procesie

Proces jest ułożony tak, jak pracuje strateg — od Odkrywania do Wdrożenia. Każdy playbook odpowiada na ten sam zestaw pytań:

- **Cel** — co ma się stać na tym etapie.
- **Decyzje** — jakie decyzje strategiczne tu zapadają.
- **Dane wejściowe** — czego potrzebujesz z poprzednich etapów.
- **Kroki** — sekwencja działań.
- **Narzędzia** — które frameworki wybrać (linki).
- **Artefakt wynikowy** — co przekazać dalej.
- **Walidacja** — skąd wiesz, że zrobiono dobrze.
- **Najczęstsze błędy** — pułapki.

## Struktura procesu

1. [[Playbooki/01 Odkrywanie|01 Odkrywanie]] — poznaj biznes, rozmówców, kontekst.
2. [[Playbooki/02 Research|02 Research]] — zbierz dane (desk + teren).
3. [[Playbooki/03 Klient|03 Klient]] — kto jest klientem, co kupuje naprawdę.
4. [[Playbooki/04 Konkurencja|04 Konkurencja]] — kto jeszcze walczy o klienta.
5. [[Playbooki/05 Rynek|05 Rynek]] — warunki rynkowe i trendy.
6. [[Playbooki/06 Pozycjonowanie|06 Pozycjonowanie]] — decyzja o miejscu w głowie/na rynku.
7. [[Playbooki/07 Komunikacja|07 Komunikacja]] — przekaz, struktura, StoryBrand.
8. [[Playbooki/08 Oferta|08 Oferta]] — co dokładnie oferujemy i za ile.
9. [[Playbooki/09 Tożsamość marki|09 Tożsamość marki]] — charakter, wartości, wizual.
10. [[Playbooki/10 Strona|10 Strona]] — gdzie strategia staje się stroną.
11. [[Playbooki/11 Treść|11 Treść]] — content zasilający komunikację.
12. [[Playbooki/12 Walidacja|12 Walidacja]] — testy przed wdrożeniem.
13. [[Playbooki/13 Wdrożenie|13 Wdrożenie]] — plan i wdrożenie.

## Zasady pracy z playbookami

1. **Nie pomijaj etapów** — każdy następny opiera się na artefakcie poprzedniego.
2. **Frameworki wybieraj świadomie** — czytaj też „kiedy NIE używać" (Zasada 3, [[02 Zasady]]).
3. **Dokumentuj artefakty** — strategia to ciąg dokumentów, nie rozmowa.
4. **Waliduj wcześnie** — lepiej wykryć błąd na etapie researchu niż pozycjonowania.
5. **Działaj iteracyjnie** — wróć do wcześniejszego etapu, gdy pojawią się nowe dane.

## Projekt i folder (standard)

Każdy projekt zakłada folder `00 Projekty/<NAZWA FIRMY>/` (agent tworzy go automatycznie w etapie 01 — [[Szablony/Struktura projektu|struktura projektu]]):

- Artefakty każdego etapu → osobne pliki `.md` (Brief, Persona, Pozycjonowanie, StoryBrand, Oferta, Tożsamość...).
- Zrzuty stron konkurencji → `Badanie/konkurencja/` (PNG + `porownanie-wizualne.md`).
- `index.html` — **przegląd projektu** (tekst + prosty CSS): stan etapów, checklista, kluczowe decyzje. **Aktualizuj po każdym etapie**.
- `DESIGN.md` — tokeny brandowe (kolory, typografia), powstaje **dopiero na etapie 09** (Tożsamość), lint WCAG.

> Zasada: folder nie jest „bałaganem" — każda nota ma miejsce. Przegląd w `index.html` pozwala zobaczyć cały projekt jednym rzutem oka.

## Wejście / wyjście całego procesu

| Wejście | Wyjście |
|---|---|
| Zlecenie/zadanie od klienta (lub własny projekt) | Kompletna strategia: pozycjonowanie, komunikacja, oferta, tożsamość, strona, content, plan wdrożenia |

Zacznij od [[Playbooki/01 Odkrywanie|01 Odkrywanie]].

---
**Zobacz też:** [[00 Start]], [[01 Jak myśli strateg marki]], [[03 Jak korzystać z OS]]

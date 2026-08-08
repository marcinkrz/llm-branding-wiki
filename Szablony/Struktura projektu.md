---
typ: szablon
użycie: każdy projekt / zlecenie
aktualizacja: 2026-08-07
---

# Struktura projektu (standard folderu)

*Jak wygląda każdy aktywny projekt w OS — folder, który agent tworzy automatycznie na starcie i utrzymuje do końca procesu. Zawiera wszystkie artefakty + przegląd (HTML) + specyfikację tokenów (DESIGN.md).*

## Lokalizacja

```
~/workspace/llm-branding-wiki/00 Projekty/<NAZWA FIRMY>/
```

> Nazwa folderu = nazwa firmy/klienta (bez spacji → użyj `-`), np. `00 Projekty/Moja-Agencja/`.

## Struktura folderu projektu

```
00 Projekty/<NAZWA>/
├── 00 Brief projektu.md          ← brief, założenia-hipotezy, plan (etap 01)
├── 01 Research klienta.md        ← segmenty, joby, persona, VoC (etap 03)
├── 02 Konkurencja.md             ← mapa rywali, profile, luki (etap 04)
├── 03 Rynek.md                   ← PESTEL, trendy, wielkość (etap 05)
├── 04 Pozycjonowanie.md          ← oświadczenie + one-liner (etap 06)
├── 05 Komunikacja.md             ← StoryBrand, ton, treści (etap 07)
├── 06 Oferta.md                  ← wartość, zakres, cena, CTA (etap 08)
├── 07 Tożsamość.md               ← osobowość, essence, kierunek ID (etap 09)
├── 08 Strona.md                  ← struktura, teksty, UX (etap 10)
├── 09 Content.md                 ← plan tematów, lejek (etap 11)
├── 10 Walidacja.md               ← hipoteza, test, próg sukcesu (etap 12)
├── 11 Wdrożenie.md               ← plan, role, metryki (etap 13)
│
├── Badanie/                       ← materiały researchowe
│   └── konkurencja/               ← zrzuty stron rywali (PNG) + porównanie
│       ├── 01-Nazwa-rywala.png
│       ├── ...
│       └── porownanie-wizualne.md ← tabela: look&feel, kolory, ton, URL, data
│
├── index.html                     ← przegląd procesu (dla stratega; aktualizowany po KAŻDYM etapie)
│                                    linki do .md, status etapów, checklista, hipotezy
├── prezentacja.html               ← wizualizacja strategii DLA KLIENTA (generowana na końcu)
│                                    same decyzje + oferta + tożsamość, BEZ linków do .md
└── DESIGN.md                      ← tokeny brandowe (POWSTAJE na etapie 09, Tożsamość)
```

## index.html — przegląd procesu

Cel: **jedna strona, na której widać stan całego projektu** — co zrobione, co w toku, co pozostało.

- Przekrój: sekcje = etapy 01–13, każdy z listą artefaktów i linkami do plików `.md`.
- Sekcja „Status" z checklistą (✓ zrobione / ○ w toku / □ do zrobienia).
- Sekcja „Kluczowe decyzje" (one-liner, segment, oferta) — szybki przegląd bez otwierania notatek.
- **Tryb: sam tekst + prosty CSS** (system font, bez obrazków) — szybki do przeglądu i druku.
- Aktualizacja: **po każdym etapie** (agent aktualizuje plik, gdy dodaje artefakt).

## prezentacja.html — wizualizacja strategii DLA KLIENTA

Cel: **jedna, samowystarczalna strona, którą pokazujesz klientowi** — łatwa do „strawienia" w 2 minuty.

- **Odbiorca:** klient (nie strateg). Dlatego: same decyzje + oferta + tożsamość, **BEZ linków do `.md`**, bez statusu procesu i bez adnotacji „hipoteza H4 / do walidacji" (to wewnętrzne).
- **Zawartość (mapowanie artefakt→sekcja):** hero = one-liner z `04 Pozycjonowanie`; Dla kogo = `01/03`; Z czym wygrywamy = `04` (oświadczenie + vs rywale); Jak pomagamy = `05/08`; Oferta = `06` (pakiety + ceny + gwarancje); Tożsamość = `07` + `DESIGN.md`; Co dalej = `11/12`.
- **Szablon:** [[Szablony/prezentacja.html|Szablony/prezentacja.html]] (instrukcja mapowania w komentarzu na górze pliku).
- **Kolory/typografia:** zawsze podmień zmienne CSS `:root` na tokeny z `DESIGN.md` (etap 09).
- **Przycisk „Drukuj / PDF"** działa przez `@media print` (ukrywa pasek i cienie).
- **Kiedy tworzyć:** na końcu procesu (po etapie 09, gdy są tokeny i oferta). Można iterować.
- Przykład referencyjny: `00 Projekty/Visual-Label/prezentacja.html`.

> Zasada: `index.html` = **proces** (dla Ciebie), `prezentacja.html` = **wynik** (dla klienta). Nie mieszaj ich.

## DESIGN.md — tokeny brandowe (etap 09+)

Cel: **jedno źródło wartości wizualnych** wypracowanych w tożsamości — do przekazania projektantom/developerom.

- Powstaje TYLKO po etapie 09 (moodboard, kolory, typografia) — wcześniej nie ma czego specować.
- Format: spec `DESIGN.md` (YAML tokens + markdown rationale) — zgodny ze skillem `design-md` (autorowanie/lint/eksport tokenów).
- Zawiera: kolory (bazowe, akcent, neutralne), typografia (h1–body), zaokrąglenia/spacery, komponenty bazowe (przycisk).
- Walidacja kontrastu przez linter WCAG (przed przekazaniem).
- Role: most między strategią a wykonaniem (strona, realizacja, identyfikacja).

---
**Uwaga:** folder tworzy agent automatycznie na starcie projektu (`00 Projekty/<firma>/`). Nie twórz go ręcznie — wystarczy użyć [[Prompty/Master prompt strategia|master prompta]] lub [[Prompty/Etap 01 Odkrywanie|promptu 01]].

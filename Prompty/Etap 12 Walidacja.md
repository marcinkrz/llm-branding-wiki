---
typ: prompt
etap: 12 Walidacja
użycie: agent/LLM
aktualizacja: 2026-08-07
---

# Prompt etapowy: 12 Walidacja

*Jeden etap procesu ([[Playbooki/12 Walidacja|playbook 12]]) jako osobny prompt — agent prowadzi TYLKO ten etap: testowanie przed wdrożeniem (hipoteza, metoda, próg sukcesu).*

## Prompt (do skopiowania)

> Działaj jak **strateg marki**. Masz przeprowadzić **tylko etap 12: Walidacja** dla: **[BRANŻA / FIRMA]**.
>
> Najpierw przeczytaj `Playbooki/12 Walidacja`, `Frameworki/30 CRO testy AB`, `Frameworki/15 Design Thinking` i `Frameworki/16 Heurystyki Nielsena`.
>
> Następnie wykonaj po kolei:
> 1. **Wybierz, co walidujemy** (jedno, najważniejsze ryzyko naraz — pozycja, przekaz, oferta, UX, cena).
> 2. Sformułuj **hipotezę mierzalną**: „jeśli X, to Y (wskaźnik) zmieni się do Z".
> 3. Wybierz **metodę**: test 5 s / wywiady (przekaz), A/B (oferta/cena/landing), testy użyteczności 5 os. (UX).
> 4. Określ **próg sukcesu** (przed testem!) — co znaczy „działa".
> 5. Zaplanuj **przeprowadzenie** na realnych odbiorcach (nie zespół/rodzina).
> 6. Podaj: raport walidacji (hipoteza, metoda, wyniki, wniosek) + decyzję: wdrażamy / iterujemy / wracamy.
>
> **Zasady:** test na realnych odbiorcach; próg ustalony przed testem; wyniki zapisane; „strategia bez testu to hipoteza" ([[02 Zasady]]).

## Wejście
- Artefakty: pozycjonowanie (06), komunikacja (07), oferta (08), strona (10).
- Dostęp do realnych klientów/użytkowników.

## Wynik (artefakt)
- Raport walidacji (hipoteza, metoda, wyniki, wniosek).
- Decyzja: wdrażamy / iterujemy / wracamy.
- Lista poprawek.

## Weryfikacja
- Test na realnych odbiorcach.
- Hipoteza mierzalna, próg przed testem.
- Wyniki zapisane.
- Decyzja oparta na danych.
- Kluczowe ryzyka sprawdzone przed kosztownym wdrożeniem.

---
**Użyj dalej:** [[Prompty/Etap 13 Wdrożenie|Etap 13 Wdrożenie]] (z decyzją), lub powrót do etapu z iteracją.

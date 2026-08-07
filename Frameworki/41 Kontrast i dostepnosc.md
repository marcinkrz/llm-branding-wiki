---
typ: framework
autor: WCAG / design dostępny
etap: Design / Strona / UX
aktualizacja: 2026-08-07
źródło: WCAG 2.1, „Contrast Minimum" (W3C) — https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html
---

# Kontrast i dostępność (WCAG)

> **Pytanie przewodnie:** Czy treść jest czytelna dla wszystkich użytkowników — w tym słabowidzących, na mobile, przy słonecznym ekranie — i czy projekt nie wyklucza części rynku?

## Co rozwiązuje

Projekt „ładny dla wypoczętego oka z dużym monitorem" — nieczytelny dla realnych użytkowników. Kontrast (stosunek jasności tekstu do tła) i ogólna dostępność (WCAG 2.x/3.x: rozmiary, touch targety, fokus, alt) podnoszą czytelność, zasięg i ułatwiają odbiór. To również aspekt prawno-biznesowy (EEA, dyrektywa dostępności, roszczenia).

## Jakie ma ograniczenia

- Dostępność to system (kontrast to tylko jeden element: fokus, nawigacja, alt-er).
- Spełnienie WCAG nie gwarantuje dobrego UX (to minimum, nie pełnia).
- Proces jest techniczny — wymaga testów (audyt, narzędzia).
- „Ogólne zasady" mogą kolidować ze brandingiem wizualnym — trzeba balansować.

## Kiedy warto ją stosować

- Gdy projektujesz stronę, aplikację, komunikaty (od początku!).
- Gdy audytujesz istniejące: kontrast tekstów, touch targety, fokus.
- Gdy pracujesz dla sektora publicznego / dużych brandów (wymogi).
- Gdy chcesz uniknąć wykluczenia (większa grupa realnych użytkowników).

## Kiedy lepiej wybrać inne podejście

- Gdy nie masz jeszcze treści/struktury → najpierw strategia (StoryBrand itd.).
- Gdy audytujesz UX całościowo → [[Frameworki/16 Heurystyki Nielsena|NN/g]].
- Gdy testujesz konwersję → [[Frameworki/30 CRO testy AB|CRO / A/B]].

## Z czym dobrze się łączy

- [[Frameworki/37 Tarcie uzytkownika|Tarcie]] — dostępność zmniejsza tarcie dla wszystkich.
- [[Frameworki/40 Hierarchia wizualna|Hierarchia]] — kontrast buduje hierarchy.
- [[Frameworki/16 Heurystyki Nielsena|NN/g]] — czytelność jako zasada UX.
- [[Frameworki/38 Kolor w brandingu|Kolor]] — paleta musi przejść kontrast.

## Jakie decyzje pomaga podjąć

- Jakie minimum kontrastu dla tekstów (WCAG AA: 4.5:1; duże: 3:1).
- Jakie rozmiary/cele dotykowe (min. 24–44 px).
- Jak poprowadzić fokus i nawigację klawiaturą.
- Jak zoptymalizować paletę pod dostępność (bez utraty charakteru).

## Jakie dane wejściowe są potrzebne

- Obecny projekt (kolory, typografia, layout).
- Narzędzia audytu kontrastu (np. axe, WebAIM contrast, silniki).
- Typ odbiorców (mobile/słabowidzący/klawiatura — realne scenariusze).

## Jaki artefakt jest wynikiem

- Audyt dostępności: lista naruszeń z priorytetem.
- Poprawki (kontrast, rozmiary, fokus, alt).
- Zasady/zestaw dla nowych projektów (design system dostępny).

## Jak zweryfikować jakość wyniku

- Kontrast tekstów ≥ WCAG AA (sprawdzenie narzędziem).
- Nawigacja klawiaturą działa (fokus widoczny).
- Treść czytelna na mobile i przy słońcu (test realny).
- Audyt ponowny pokazuje poprawę (nie regres).

## Typowe błędy początkujących

- Kontrast „na oko" bez pomiaru (wygląda dobrze, a nie spełnia AA).
- Ignorowanie fokusa/touch targetów (tylko kolory).
- Traktowanie dostępności jako „dodatku" na końcu (kosztowna poprawka).
- Konflikt „brandowy kolor" z kontrastem — brak alternatyw dla tekstu (ciemniejszy odcień).

## Pytania do klienta

- „Czy nasza strona spełnia WCAG AA dla kontrastu tekstu?"
- „Czy da się obsłużyć klawiaturą (fokus widoczny)?"
- "Czy poprawa dostępności to u nas polityka, czy 'kiedyś'?"

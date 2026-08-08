---
typ: indeks
aktualizacja: 2026-08-07
---

# Prompty

*Prompty do uruchamiania agenta (LLM) jako **aktywnego konsultanta marki** — nie chatbota odpowiadającego na pytania, ale procesu prowadzącego od zlecenia do strategii.*

## Dostępne prompty

| Prompt | Do czego |
|---|---|
| [[Prompty/Master prompt strategia\|Master prompt strategia]] | Pełny proces od zlecenia do strategii — **z gate'm discovery** (tryb A: masz dane / tryb B: agent pyta) |
| [[Prompty/Master prompt z danymi klienta\|Master prompt z danymi klienta]] | Gdy **masz wypełniony kwestionariusz/materiały klienta** — wklejasz dane razem z promptem, agent buduje z faktów |
| **Etapowe (01–13)** | Praca iteracyjna: agent prowadzi TYLKO jeden etap, pyta, dostarcza artefakt |
| → [[Prompty/Etap 01 Odkrywanie\|01 Odkrywanie]] | Brief, założenia-hipotezy, plan researchu |
| → [[Prompty/Etap 02 Research\|02 Research]] | Plan i porządkowanie badania (fakty vs. opinie) |
| → [[Prompty/Etap 03 Klient\|03 Klient]] | Segmenty, joby (JTBD), persona, język klienta |
| → [[Prompty/Etap 04 Konkurencja\|04 Konkurencja]] | Prawdziwi rywale, mapa, luki |
| → [[Prompty/Etap 05 Rynek\|05 Rynek]] | Wielkość, trendy (PESTEL), ryzyka |
| → [[Prompty/Etap 06 Pozycjonowanie\|06 Pozycjonowanie]] | Kluczowa decyzja: kategoria, przewaga, dowód |
| → [[Prompty/Etap 07 Komunikacja\|07 Komunikacja]] | StoryBrand, przekaz, ton, treści |
| → [[Prompty/Etap 08 Oferta\|08 Oferta]] | Wartość, zakres, stack, gwarancja, cena, CTA |
| → [[Prompty/Etap 09 Tożsamość marki\|09 Tożsamość marki]] | Osobowość, essence, kierunek wizualny (brief) |
| → [[Prompty/Etap 10 Strona\|10 Strona]] | Struktura, teksty, UX, CTA, tarcie |
| → [[Prompty/Etap 11 Treść\|11 Treść]] | Plan contentu, lejek, kanały, metryki |
| → [[Prompty/Etap 12 Walidacja\|12 Walidacja]] | Hipoteza, metoda, próg sukcesu (testy) |
| → [[Prompty/Etap 13 Wdrożenie\|13 Wdrożenie]] | Plan, briefy wykonawcze, pomiar, iteracje |

## Jak używać

Masz **trzy ścieżki** — wybierz według tego, ile danych masz na starcie:

**Ścieżka 1 — masz dane klienta (ZALECANA dla realnego zlecenia).**
Klient wypełnił kwestionariusz discovery / masz notatki z rozmowy / materiały firmy.
→ Użyj [[Prompty/Master prompt z danymi klienta|master prompta z danymi klienta]] i **wklej dane razem z promptem**. Agent buduje z faktów, pyta tylko o krytyczne braki.

**Ścieżka 2 — nie masz danych, chcesz całość naraz.**
→ Użyj [[Prompty/Master prompt strategia|master prompta]] (tryb B). Agent ma teraz **gate discovery**: wypisze braki, zada pytania i **zatrzyma się** do Twojej odpowiedzi, zanim zacznie generować.

**Ścieżka 3 — etapami (największa kontrola, do dużej strategii).**
→ Zacznij od [[Prompty/Etap 01 Odkrywanie|etapu 01]], po każdym etapie weryfikuj wynik, potem przechodź dalej (linki „Użyj dalej"). Każdy prompt etapowy sam wymusza pętlę pytań.

1. Agent powinien najpierw przeczytać [[01 Jak myśli strateg marki]] i [[03 Jak korzystać z OS]].
2. Na końcu zweryfikuj [[Checklisty/Checklista jakości strategii|checklistą jakości]] i [[Checklisty/Checklista wdrożenia|wdrożenia]].

> **Lekcja z praktyki (2026-08):** master prompt *bez* gate'u discovery przeszedł cały proces bez zadania pytań i wygenerował strategię na samych hipotezach. Dlatego ścieżka 1 (dane na wejściu) daje najlepszy wynik — zob. [[Audyt Brand Strategy OS]].

## Zasady budowy prompty
- Prompt definiuje **proces**, nie wynik „od razu".
- Agent **pyta**, gdy brakuje danych (nie zgaduje).
- Każdy artefakt ma źródło danych (Zasada „opinie ≠ fakty").
- Na końcu: kompletna strategia + plan wdrożenia.

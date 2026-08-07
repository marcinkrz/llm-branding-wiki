---
typ: indeks
aktualizacja: 2026-08-07
---

# Prompty

*Prompty do uruchamiania agenta (LLM) jako **aktywnego konsultanta marki** — nie chatbota odpowiadającego na pytania, ale procesu prowadzącego od zlecenia do strategii.*

## Dostępne prompty

| Prompt | Do czego |
|---|---|
| [[Prompty/Master prompt strategia\|Master prompt strategia]] | Pełny proces od zlecenia do strategii (dla dowolnej branży) |
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

**Opcja A — całość naraz:** skopiuj [[Prompty/Master prompt strategia|master prompt]] i wstaw nazwę branży/klienta. Agent przejdzie przez cały proces.

**Opcja B — etapami (zalecane przy dużej strategii):** zacznij od [[Prompty/Etap 01 Odkrywanie|etapu 01]], po każdym etapie weryfikuj wynik, potem przejdź do następnego (linki „Użyj dalej" na dole każdego prompta).
1. Agent powinien najpierw przeczytać [[01 Jak myśli strateg marki]] i [[03 Jak korzystać z OS]].
2. Na końcu zweryfikuj [[Checklisty/Checklista jakości strategii|checklistą jakości]] i [[Checklisty/Checklista wdrożenia|wdrożenia]].

## Zasady budowy prompty
- Prompt definiuje **proces**, nie wynik „od razu".
- Agent **pyta**, gdy brakuje danych (nie zgaduje).
- Każdy artefakt ma źródło danych (Zasada „opinie ≠ fakty").
- Na końcu: kompletna strategia + plan wdrożenia.

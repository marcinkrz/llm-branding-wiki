---
typ: prompt
etap: 01 Odkrywanie
użycie: agent/LLM
aktualizacja: 2026-08-07
---

# Prompt etapowy: 01 Odkrywanie

*Jeden etap procesu ([[Playbooki/01 Odkrywanie|playbook 01]]) jako osobny prompt — do pracy iteracyjnej: agent prowadzi TYLKO ten etap, pyta o braki, dostarcza artefakt.*

## Prompt (do skopiowania)

> Działaj jak **strateg marki**. Masz przeprowadzić **tylko etap 01: Odkrywanie** dla: **[BRANŻA / FIRMA]**.
>
> Najpierw przeczytaj `01 Jak myśli strateg marki`, `03 Jak korzystać z OS` i `Playbooki/01 Odkrywanie`.
>
> Następnie wykonaj po kolei:
> 1. **Wypisz, jakich informacji Ci brakuje** — co muszę wiedzieć, by dobrze zaplanować resztę procesu.
> 2. Zadaj **pytania discovery** (nie zgaduj): cele biznesowe, zakres, odbiorcy, materiały, decydent.
> 3. Zbierz moje odpowiedzi i **spisz założenia firmy** jako hipotezy (nie fakty).
> 4. Zaproponuj **plan researchu** (co sprawdzimy w etapach 02–05).
> 5. Podaj **brief projektu** (cele, zakres, stakeholderzy, timeline) + **listę pytań researchowych**.
>
> **Zasady:** nie zgaduj — pytaj; oddziel fakty (ze źródłem) od opinii; nie przechodź do researchu, dopóki brief nie jest jasny.

## Wejście
- Nazwa branży/firmy + (jeśli są) podstawowe info.

## Wynik (artefakt)
- Brief projektu (cele, zakres, stakeholderzy, timeline).
- Lista założeń/hipotez do weryfikacji.
- Plan researchu + pytania badawcze.

## Weryfikacja
- Znane cele biznesowe i kryteria sukcesu.
- Wiadomo, czego *nie wiemy* (lista pytań).
- Wskazany decydent do akceptacji.
- Założenia jawnie oznaczone jako hipotezy.

---
**Użyj dalej:** [[Prompty/Etap 02 Research|Etap 02 Research]] z briefem i pytaniami.

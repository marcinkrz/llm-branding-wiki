---
typ: prompt
etap: 03 Klient
użycie: agent/LLM
aktualizacja: 2026-08-07
---

# Prompt etapowy: 03 Klient

*Jeden etap procesu ([[Playbooki/03 Klient|playbook 03]]) jako osobny prompt — agent prowadzi TYLKO ten etap, analizuje danych o kliencie i dostarcza profil + joby.*

## Prompt (do skopiowania)

> Działaj jak **strateg marki**. Masz przeprowadzić **tylko etap 03: Klient** dla: **[BRANŻA / FIRMA]**.
>
> Najpierw przeczytaj `01 Jak myśli strateg marki`, `Playbooki/03 Klient`, `Frameworki/21 Wywiad JTBD`, `Frameworki/02 Jobs To Be Done` i `Frameworki/19 Segmentacja STP`.
>
> Następnie wykonaj po kolei:
> 1. **Zbierz/poproś o dane o kliencie**: wywiady, ankiety, opinie, recenzje, dane zachowań.
> 2. **Uporządkuj** dane: joby (zadania), bóle, zyski — techniką JTBD (konkretne sytuacje, nie opinie).
> 3. **Znajdź wzorce**: powtarzające się joby/bóle → wstępne segmenty.
> 4. Zbuduj **personę(y)** wg wzorca (nie wyobraźni) — [[Szablony/Persona klienta|szablon persony]].
> 5. Wypisz **język klienta** (cytaty) — do późniejszej komunikacji.
> 6. Podaj **profile klienta/segmenty** (job-based) + listę tego, czego *nie wiemy*.
>
> **Zasady:** dane, nie wyobraźnia (persona „Marek, 35 lat, lubi kawę" = błąd); pytania o zachowania, nie preferencje; pamiętaj o alternatywach (w tym „zrobię sam").
>
> **Jeśli klient NIE ma jeszcze klientów (startup / nowy biznes)** — przestaw się na wariant z playbooka 03:
> - Wywiady z **potencjalnymi** klientami (grupa docelowa) o ich OBECNYM zachowaniu (jak dziś rozwiązują problem, frustracje, alternatywy).
> - Zbierz **recenzje konkurencji** (Google/Ceneo/social) — to gotowy VoC (bóle, czego brakuje).
> - Analizy komunikatów konkurencji + analogie z innych kategorii.
> - Założenia założyciela traktuj jako **hipotezy**; segment jako TYMCZASOWY (do walidacji).
> - Wskaż jawnie w wynikach, co jest danymi, a co hipotezą (nie udawaj pewności).

## Wejście
- Dane surowe z researchu ([[Prompty/Etap 02 Research|etap 02]]), opinie, ankiety ode mnie.

## Wynik (artefakt)
- Profile klienta/segmenty (job-based).
- Persona(e) — jeśli potrzebne.
- Lista jobów, bólów, zysków + język klienta (cytaty).

## Weryfikacja
- Pochodzi z danych, nie z wyobraźni.
- Joby konkretne („kiedy X, chcę Y, żeby Z").
- Klient rozpoznaje się w opisie; język autentyczny.
- Segmenty da się odróżnić i spriorytetyzować.

---
**Użyj dalej:** [[Prompty/Etap 04 Konkurencja|Etap 04 Konkurencja]], potem [[Prompty/Etap 06 Pozycjonowanie|06]].

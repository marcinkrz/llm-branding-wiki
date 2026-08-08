---
typ: audyt
aktualizacja: 2026-08-08
status: analiza niezależna (branch roboczy — NIE scalać z main bez decyzji właściciela)
---

# Audyt Brand Strategy OS

*Niezależny przegląd całego OS (rdzeń, playbooki, frameworki, prompty, szablony, checklisty) + analiza realnej sesji użycia („Strategia marki Visual Label", model deepseek-v4-flash). Cel: zweryfikować poprawność merytoryczną, ocenić, czy framework wydobywa przydatne informacje, i zdiagnozować, dlaczego w praktyce nie zadał pytań.*

---

## 1. Podsumowanie (TL;DR)

**Framework jest merytorycznie poprawny i dobrze zaprojektowany.** Treści playbooków i frameworków są zgodne z kanonem strategii marki (Ries/Trout, Dunford, Miller, Aaker, JTBD, STP) i — co ważniejsze — zawierają to, czego brakuje w typowych wiki: *kiedy NIE używać*, *typowe błędy*, *jak walidować*. To realnie wydobywa przydatne informacje, **ale tylko pod warunkiem, że agent dostanie dane wejściowe od człowieka.**

**Główna wada jest procesowa, nie merytoryczna:** master prompt *mówi* „zadaj pytania", ale tego **nie wymusza**. W efekcie w sesji Visual Label agent przeszedł 13 etapów bez zadania ani jednego pytania i zbudował strategię na oznaczonych hipotezach. To przewidywalne zachowanie LLM-a: gdy prompt nie wstrzyma go na starcie, „przejdzie proces" syntetycznie.

**Naprawa jest prosta i już wykonana na tym branchu:**
- master prompt dostał **twardy gate discovery** (nie wolno zaczynać bez danych wejściowych lub bez rozmowy Q&A),
- dodany **wariant „z danymi klienta"** (wklejasz wypełniony kwestionariusz → agent od razu robi strategię z faktów),
- kwestionariusz discovery uzupełniony o sekcję dla **nowego biznesu** (dotychczasowy zakładał istniejących klientów).

---

## 2. Czy informacje w OS są prawdziwe? (weryfikacja merytoryczna)

Sprawdziłem rdzeń, losowo i celowo wybrane playbooki (01 Odkrywanie, 06 Pozycjonowanie) oraz frameworki (StoryBrand) względem źródeł i powszechnej praktyki branżowej.

### Co jest poprawne ✅

| Obszar | Ocena |
|---|---|
| **Sposób myślenia stratega** (fakty vs. opinie, hipotezy H1..Hn, pułapki poznawcze) | Zgodne z dobrą praktyką researchu i metodologii JTBD. Bardzo mocny dokument. |
| **Struktura procesu 01→13** (Odkrywanie→Research→Klient/Konkurencja/Rynek→Pozycjonowanie→…→Walidacja→Wdrożenie) | Zgodna z procesami agencji (discovery → research → positioning → validation → implementation). |
| **Karty frameworków** (StoryBrand, pozycjonowanie Ries/Trout, Market Positioning Canvas/Dunford, CBBE Kellera, Aaker) | Merytorycznie trafne, z poprawnym przypisaniem autorów i źródłami. Nie znalazłem błędów faktograficznych. |
| **Sekcje „kiedy NIE używać" i „typowe błędy"** | To wyróżnik — część „storybrand upraszcza, nie decyduje o pozycjonowaniu" jest trafna i rzadka w darmowych materiałach. |
| **Rozdzielenie wiedzy / frameworków / playbooków / szablonów / promptów / checklist** | Zdrowa architektura (Zasada 4). |

### Drobne niedokładności / rzeczy do doprecyzowania ⚠️

1. **W niektórych kartach brakuje twardej walidacji liczbowej** (np. „wielkość rynku" w playbooku 05 nie wskazuje, skąd brać dane w PL — GUS, raporty branżowe, PMR, Statista). Dla solo-stratega bez dostępu do płatnych raportów to realna luka.
2. **Archetypy marki (karta 17)** — podstawa naukowa jest dyskusyjna (Jung w zastosowaniu marketingowym to bardziej heurystyka niż nauka). OS to sygnalizuje („jeśli ma sens"), ale można mocniej oznaczyć jako *narzędzie inspiracji, nie dowód*.
3. **„How Brands Grow" (karta 08)** — tezy Sharpa (mental + physical availability, wzrost przez penetrację, nie lojalność) są poprawne, ale warto dodać zastrzeżenie: model bywa krytykowany za słabe dopasowanie do B2B/małych nisz lokalnych — co dotyczy bezpośrednio Visual Label.

**Werdykt:** nie znalazłem informacji fałszywych. Są pojedyncze miejsca, gdzie warto dodać kontekst lub źródło danych — szczegóły w sekcji 5.

---

## 3. Czy framework wydobywa przydatne informacje?

**Tak — ale warunkowo.** Framework ma w sobie wszystkie narzędzia do wydobycia wartościowych insightów:

- kwestionariusz discovery (21 pytań o konkret i biznes, nie o „jakie kolory lubisz"),
- playbook 03 Klient (JTBD, persona, język klienta „z danych, nie z wyobraźni"),
- playbook 04 Konkurencja (rywale *z perspektywy klienta*, luki),
- wariant „nowy biznes" (recenzje konkurencji jako VoC, hipotezy do walidacji).

**Problem:** framework *umożliwia* wydobycie, ale w master promptcie go **nie wymusza**. W sesji Visual Label:

- **1 wiadomość użytkownika** (sam master prompt) → **10 wiadomości asystenta** → commit `62de15b` z kompletną strategią.
- Etap 01 („Odkrywanie — zadaj pytania, nie zgaduj") został wykonany **deklaratywnie**: agent wypisał brief i „hipotezy", ale nie zadał Ci żadnego pytania.
- Wszystkie decyzje o segmencie, cenie, geografi, przewadze są oznaczone jako hipotezy H1..Hn — **bo agent nie miał żadnych faktów wejściowych.** To nie zły output, to *jedyny możliwy* output przy braku danych.

Wniosek: **Twoja intuicja jest trafna.** Gdyby master prompt dostał wypełniony kwestionariusz + materiały klienta, strategia byłaby zbudowana z faktów, a nie z hipotez do późniejszej walidacji.

---

## 4. Dlaczego master prompt nie zadawał pytań (analiza przyczyny)

Porównałem master prompt z promptem etapowym 01 — i to jest źródło problemu:

| | Prompt etapowy 01 Odkrywanie | Master prompt |
|---|---|---|
| Wymuszenie pytań | **„nie przechodź do researchu, dopóki brief nie jest jasny"** — twardy warunek | „Zadaj pytania (jeśli nie masz odpowiedzi)" — miękka sugestia |
| Dane wejściowe | „Nazwa branży + (jeśli są) podstawowe info" | brak — tylko placeholder `[BRANŻA/FIRMA]` |
| Tryb | iteracyjny, jeden etap | „całość naraz" |
| Zachęta do pętli Q&A | explicit | brak |

**Mechanizm błędu:** LLM w trybie „zrób całość naraz" optymalizuje pod *ukończenie zadania*. Gdy prompt nie zablokuje mu drogi, wygeneruje pełną strukturę — wypełniając luki hipotezami. To zgodne z instrukcją „nie zgaduj, oznacz jako hipotezę", tyle że *najlepiej* oznaczonych hipotez jest dużo mniej niż faktów.

Dodatkowo master prompt:
- nie mówi **jakie konkretnie** dane są *niezbędne* na starcie (cele, segment, klienci, konkurencja, ceny, „czego nie chcę"),
- nie rozróżnia **dwóch trybów pracy**: (A) mam dane klienta / (B) muszę przeprowadzić discovery,
- nie każe **wstrzymać proces** do czasu rozmowy.

---

## 5. Co bym dodał / zmienił (rekomendacje)

### Priorytet 1 — proces (już wdrożone na tym branchu)
- **Twardy gate discovery w master promptcie** — nie wolno zaczynać bez danych wejściowych lub bez rozmowy Q&A. *(zrobione)*
- **Wariant „z danymi klienta"** — osobny prompt, do którego wklejasz wypełniony kwestionariusz. *(zrobione)*
- **Kwestionariusz discovery + sekcja nowy-biznes** (potencjalni klienci, „za co by zapłacili", status landinga W0). *(zrobione)*

### Priorytet 2 — merytoryka (propozycje, do Twojej decyzji)
- **Playbook 05 Rynek:** dodać konkretne, darmowe źródła danych dla PL (GUS, CEIDG, raporty branżowe, Google Trends, fora/grupy FB branżowe) — solo-strateg nie ma Statista.
- **Karta 17 Archetypy:** mocniejsze zastrzeżenie „inspiracja, nie dowód naukowy".
- **Playbook 03 Klient:** dodać *minimalną liczbę rozmów VoC* (np. „5–8 wywiadów z potencjalnymi klientami zanim zapiszesz język klienta") — inaczej „język klienta" powstaje z jednej rozmowy lub z wyobraźni.
- **Checklista jakości:** dodać punkt wejściowy *„Czy na starcie odbyło się discovery (kwestionariusz/rozmowa)? Jeśli nie — reszta jest hipotezą."* (obecnie checklista zaczyna się od segmentu, pomijając warunek wejścia).

### Priorytet 3 — brakujące elementy (światowa praktyka, której OS nie ma)
1. **Brand audit istniejącej marki** — OS zakłada albo nowy biznes, albo strategię „od zera". Brakuje playbooka dla *rebranding istniejącej firmy* (audyt obecnych touchpointów, co zostawić/co wyciąć). To częsty przypadek klienta agencji.
2. **Pomiar po wdrożeniu** — karta 53 Pomiar marki istnieje, ale playbook 13 Wdrożenie mógłby mocniej powiązać metryki z pętlą (kwartalny perception check, NPS, awareness). Obecnie walidacja kończy się „przed wdrożeniem".
3. **Stakeholder/warsztat decyzyjny** — szablon warsztatu jest, ale nie ma mechaniki *gdy klient nie zgadza się z rekomendacją* (jak prezentować alternatywy, jak dokumentować decyzję klienta vs. rekomendację stratega).

---

## 6. Co NIE jest wadą (ważne rozróżnienie)

- To, że agent wygenerował strategię na hipotezach, **nie jest błędem frameworka** — to błąd *uruchomienia* go bez danych. Framework sam mówi: „nie buduj pełnej marki przed walidacją popytu".
- Hipotezy H1..Hn w projekcie Visual Label są **poprawnie oznaczone** — OS zadziałał zgodnie z zasadą „opinia bez dowodu = hipoteza".
- Proces 13-etapowy **nie jest za długi** — jest zgodny z praktyką. Problem był w tym, że przeszedł go bez pierwszego kroku (discovery z człowiekiem).

---

## 7. Pliki zmienione/dodane na tym branchu

| Plik | Zmiana |
|---|---|
| `Prompty/Master prompt strategia.md` | twardy gate discovery + 2 tryby wejścia (A: dane / B: Q&A) + reguła „zatrzymaj się i zapytaj" |
| `Prompty/Master prompt z danymi klienta.md` | **NOWY** — wariant, gdy wklejasz wypełniony kwestionariusz/materiały |
| `Szablony/Kwestionariusz discovery.md` | + sekcja „nowy biznes" (potencjalni klienci, płatność, W0) |
| `Prompty/Prompty.md` | aktualizacja hubu: 3 ścieżki (z danymi / Q&A / etapami), kiedy która |
| `Audyt Brand Strategy OS.md` | **NOWY** — ten dokument |

---

## 8. Zalecane użycie po tej audycie

1. **Dla prawdziwego klienta:** wyślij mu `Szablony/Kwestionariusz discovery` → wklej jego odpowiedzi + linki/materiały do `Master prompt z danymi klienta`. Dostaniesz strategię z faktów.
2. **Dla siebie (Visual Label):** masz już pełną strategię na hipotezach. Następny krok to **walidacja W1** (kwestionariusz `Kwestionariusz Walidacji W1-W3`) — nie kolejna iteracja prompta.
3. **Dla szybkiego researchu:** użyj promptów etapowych (01→13) zamiast mastera — wymuszają pętlę pytań na każdym kroku.

---

*Audyt wykonany na branchu `audit/strategy-os-review`. Nie scalać z `main` bez Twojej decyzji — część rekomendacji (sekcja 5, priorytety 2–3) to propozycje wymagające Twojej akceptacji.*

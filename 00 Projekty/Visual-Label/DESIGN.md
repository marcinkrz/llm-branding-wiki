---
version: alpha
name: Visual Label
description: >
  Visual Label — pewny przewodnik w budowaniu marki, która działa.
  Strategia + design + strona konwertująca, po ludzku. Baza (ink) daje powagę
  i wiarygodność; jedyny energiczny akcent (volt) napędza działanie i CTA;
  off-white zapewnia przestrzeń i czytelność. Go-to-market dla MŚP, nie galeria.
colors:
  primary: "#0E1B24"
  secondary: "#5B7083"
  accent: "#C6F23E"
  neutral: "#F6F5F2"
  on-dark: "#FFFFFF"
typography:
  h1:
    fontFamily: Space Grotesk
    fontSize: 3rem
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  h2:
    fontFamily: Space Grotesk
    fontSize: 2rem
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  body-md:
    fontFamily: Inter
    fontSize: 1.0625rem
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0em"
  label-caps:
    fontFamily: Inter
    fontSize: 0.8125rem
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.08em"
rounded:
  sm: 4px
  md: 8px
  lg: 16px
spacing:
  sm: 8px
  md: 16px
  lg: 32px
  xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "12px 20px"
    typography: "{typography.label-caps}"
  button-primary-hover:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-dark}"
  button-secondary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.md}"
    padding: "12px 20px"
  link-inline:
    textColor: "{colors.primary}"
  card:
    backgroundColor: "{colors.neutral}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  hero-title:
    textColor: "{colors.primary}"
    typography: "{typography.h1}"
  body-text-on-light:
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
  body-text-on-dark:
    textColor: "{colors.on-dark}"
    typography: "{typography.body-md}"
---

## Overview

Visual Label to studio marki i strony internetowej dla małych firm usługowych. Pozycjonowanie:
**„strategia najpierw, design po — marka i strona, które przynoszą klientów, mierzone konwersją,
z jawnym procesem i opieką."** Design ma wyglądać pewnie, czytelnie i konwertująco — dla MŚP,
nie dla galerii. Jeden energiczny akcent (volt) prowadzi do działania; baza (ink) buduje zaufanie.

## Colors

- **Primary – Ink (`#0E1B24`):** niemal-czarny granat. Nagłówki, tekst, ciemne sekcje. Powaga i strategia.
- **Secondary – Steel (`#5B7083`):** przygaszona stal do tekstu drugorzędnego, etykiet, opisów.
- **Accent – Volt (`#C6F23E`):** jedyny akcent działania — CTA, zaznaczenia, distinctive asset. Energia i konwersja.
- **Neutral – Off-white (`#F6F5F2`):** tło sekcji; zapewnia przestrzeń i ciepło (nie czysta biel „korpo").
- **On-dark (`#FFFFFF`):** tekst na ciemnym tle / przycisku.

## Typography

- **Space Grotesk** – nagłówki (h1/h2). Charakter „strategiczno-techniczny", odrębny od rywali.
- **Inter** – tekst (body) i etykiety. Czytelność. Nagłówki duże i pogrubione; układ smukły, „go-to-market".
- Zasada: nagłówki w języku korzyści („Marka i strona, które przynoszą klientów"), nie „o nas".

## Layout & Spacing

- Dużo przestrzeni (skala `xl` = 64px między blokami), jasna hierarchia, jedno zadanie na sekcję.
- Kolejność sekcji wg StoryBrand: problem → przewodnik → dowody → plan → oferta → CTA.
- Skala: sm 8 / md 16 / lg 32 / xl 64.

## Shapes

- Zaokrąglenia: sm 4 / md 8 / lg 16. Przyciski `md`, karty `lg` — spójne i przyjazne, nie „kanciasto-korpo".

## Components

- **button-primary** – volt na ink (wysoki kontrast), to jedyny „główny" przycisk na ekranie. Hover: ink/white.
- **button-secondary** – ink/white do akcji drugorzędnej.
- **link-inline** – ink, podkreślenie; kolor akcentu tylko dla podkreślenia/ikony.
- **card** – neutral, zaokrąglenie lg; tło treści i ofert.
- **hero-title / body-text** – kontrast ink na jasnym tle; wariant on-dark dla ciemnych sekcji.

## Do's and Don'ts

- **Do:** używać volt wyłącznie do działania (CTA, akcenty); dawać dużo przestrzeni; nagłówki korzyścią dla klienta; kontrast AA dla tekstu.
- **Don't:** nie rozlewać volt po całej stronie (traci rolę akcentu); nie robić „galerii kreatywnej" (mówi „drogo"); nie naśladować korpo-błękitu ani żółci rywali; nie używać szablonowego „uroku" zamiast jasności i konwersji.

---
slug: design-token
titel: Design-Token
art: system
angelegt: 2026-08-30
zuletzt: 2026-08-30
---

# Design-Token

Ein benannter Platzhalter für eine gestalterische Entscheidung — `color-text-primary`
statt `#000000` —, aus dem heraus Werte für mehrere Plattformen erzeugt werden. Die
Notation besteht **nur aus dem Namen**: Es gibt keine Klammern, keine Operatoren und
keine Fläche mit Achsen, die Bedeutung sitzt in der Reihenfolge der Wortteile. Sie
ist die jüngste Notation dieses Tagebuchs und die einzige, deren Spezifikation
während seiner Laufzeit stabil wurde.

## Kern

**Wer, wann.** Der Begriff wird durchgängig auf **2014** und auf **Jina Anne** bei
Salesforce datiert, im Zuge des Lightning Design System. Das Problem war die
Vervielfältigung: dieselbe Farbe, in mehreren Codebasen von Hand gepflegt, lief
auseinander. Dazu das Werkzeug **Theo** („an abstraction for transforming and
formatting Design Tokens"), erste Fassung von Sönke Rohde. Weiter: **Style
Dictionary** 2017 (Danny Banks, Amazon), die **Design Tokens Community Group** beim
W3C 2019, erste stabile Fassung der Spezifikation am **28. Oktober 2025**.

**Was die Spezifikation festlegt.** „A (Design) Token is information associated with
a human readable name, at minimum a name/value pair." Ein Token ist ein Objekt mit
`$value`, dazu `$type` und optional `$description`. Ein Token darf auf ein anderes
zeigen — in geschweiften Klammern, `{colors.blue}`, mit dem Punkt als Pfadtrenner.
Deshalb sind `$`, `{`, `}` und `.` in Namen **verboten**. Eine Zeichensprache, die
vier Zeichen verbietet, weil sie sie selbst braucht.

**Die Grammatik.** Nathan Curtis (EightShapes) zerlegt den Namen in Ebenen:
Namespace (System, Theme, Domäne), Objekt (Komponente, Element), Basis (Kategorie,
Konzept, Eigenschaft) und Modifikatoren (Variante, Zustand, Skala, Modus). Daraus
entstehen Namen wie `$esds-consumer-color-marquee-text-primary` oder
`$color-action-background-secondary-hover-on-dark`. Die Syntax ist reine
**Wortstellung**.

**Zwei Ebenen, und die untere ist tabu.** Primitive Tokens sagen, *was* ein Wert ist
(`blue-500`), semantische, *wozu* er dient (`action-primary`). Die Standardregel der
Literatur lautet, dass Komponenten nur die semantische Ebene referenzieren dürfen —
dann ändert ein Rebranding eine Zuordnungsdatei statt hundert Stellen. Wer die
Notation benutzt, *soll* den Wert nicht sehen.

**Der Ausgang beim Erfinder.** Salesforce empfiehlt seinen Entwicklern heute, statt
der eigenen Design-Tokens die „global styling hooks" (CSS Custom Properties) zu
benutzen — wörtlich: „Even if you aren't planning to transition to SLDS 2 yet, we
recommend that you use global color styling hooks instead of design tokens, where
possible, to align with the Web Content Accessibility Guidelines (WCAG) 2.1 color
contrast standards." Die Namen waren richtig; die Werte hinter ihnen hielten den
Kontraststandard nicht ein. Design-Tokens erhalten ab LWC-API-Version 61.0 keine
Aktualisierungen mehr, Theo wurde am **9. Juni 2025** archiviert.

## Warum das eine Notation ist (und der Zweifel daran)

Nach der Arbeitsdefinition in [[notation]]: **rechenbar** — ein Theme umschalten
heißt, eine Verweisebene neu zuzuordnen, ohne über eine einzelne Farbe nachzudenken;
**erblich** — Namensschemata werden übernommen, nicht neu verhandelt, und
Umbenennungen brauchen Umleitungstabellen (`deprecated.json` bei GitHubs Primer:
`text.primary` → `fg.default`); **mit Rand** — was kein Token hat, ist im System
nicht sagbar.

Der Zweifel bleibt: Ein Name mit einem Wert ist eine Variable, und die Grenze
zwischen Notation und bloßer Benennung ist hier so unscharf wie sonst nirgends im
Tagebuch. Was den Ausschlag gibt, ist die Referenzsyntax und die Wortstellungs-
grammatik — nicht das Name/Wert-Paar für sich.

## Belegt / vermutet

- **Belegt:** Definition, `$value`/`$type`, Klammer-Referenz und die verbotenen
  Zeichen (Design Tokens Format Module 2025.10) · Datum der stabilen Fassung,
  28.10.2025 (W3C-Ankündigung) · Theos Selbstbeschreibung und die Archivierung am
  09.06.2025 (GitHub) · die WCAG-Empfehlung wörtlich (Salesforce-Entwicklerdoku) ·
  Curtis' Ebenen und Beispielnamen (EightShapes).
- **Vermutet / schwach belegt:** Die Datierung **2014** und die Zuschreibung an Jina
  Anne stammen aus Sekundärdarstellungen; ihre eigene Projektseite nennt kein Jahr,
  eine Primärquelle von 2014 habe ich nicht gesehen. Ebenso sekundär: Style
  Dictionary 2017, Community Group 2019.
- **Nicht geprüft:** ob es einen dokumentierten Einzelfall gibt, in dem ein Token
  seinen Namen behielt und der Name durch einen Wertwechsel falsch wurde.

## Verwandt

- [[selbstverdeckung]] — der Fall, der die Richtung des Musters umdreht: hier
  verdeckt das Zeichen den Wert, nicht das Ergebnis das Zeichen
- [[notation]] — Grenzfall zur bloßen Benennung; prüft alle drei Eigenschaften
- [[uniformer-irrtum]] — reine Selbstschlüsselung (der Name *ist* die Legende) und
  trotzdem nur für die Bedeutung, nie für den Wert
- [[adressierbarkeit]] — offene Frage: Ist ein hierarchischer Namensraum eine
  Dimension, in die man zeigen kann?
- [[werkzeugzwang]] — bisher unberührt: Was hat das Werkzeug (Figma, Style
  Dictionary, CSS Custom Properties) an dieser Notation geformt?
- [[tabellenblatt]] — die Umkehrung im selben Feld: dort Wert über Formel, hier Name
  über Wert

## Kommt vor in

- `entries/2026/2026-08-30.md`

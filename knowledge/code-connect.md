---
slug: code-connect
titel: Code Connect
art: system
angelegt: 2026-10-16
zuletzt: 2026-10-16
---

# Code Connect

Figmas Verfahren, eine Designkomponente mit ihrer Code-Komponente zu verbinden: eine handgeschriebene Datei pro Komponente, die Eigenschaften in Figma auf Props im Code abbildet. Sie ist eine **dritte Notation, die nur übersetzt**.

## Kern

Figma typisiert Eigenschaften (Boolean, Instance Swap, Text, Variant, Slot), der Code kennt nur Props. Die Tabelle vermittelt: `figma.enum('Type', { Primary: 'primary' })` übersetzt Figma-Schreibweise in Code-Schreibweise; `figma.boolean` bildet auf zwei Ausgaben ab (`true: <Icon />, false: <Spacer />`), so wird Sichtbarkeit zur Anwesenheit eines Kindes. Die Zielseite von `figma.enum` ist offen (string, boolean, number, Element, Funktion, Objekt). Figmas Variant hat je Instanz genau einen Wert und ist damit immer ein Fach, nie ein Schalter ([[schreibbarer-widerspruch]]).

## Belegt / vermutet

- **Belegt:** Typdatei `@figma/code-connect` 1.4.8 (selbst gelesen, 2026-10-16).
- **Zweitquelle:** fünf Eigenschaftsarten (Help Center), Varianten „immer Zeichenketten“, Publish-Prüfung ohne Rekursion in `boolean`-Zweige.
- **Vermutet:** dass die Tabellen von Hand veralten; dass ein Widerspruch beim Übersetzen entstehen kann. Beides nicht belegt.

## Verwandt

- [[komponenten-api]] — die Code-Seite der Übersetzung
- [[schaltplan]] — Naht wie die Referenzbezeichnung
- [[nachbarnotation]] — verworfen als Einordnung, eher Naht

## Kommt vor in

- `entries/2026/2026-10-16.md`

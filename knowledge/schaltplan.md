---
slug: schaltplan
titel: Schaltplan (mit Stückliste)
art: system
angelegt: 2026-09-17
zuletzt: 2026-09-17
---

# Schaltplan (mit Stückliste)

Der elektrische Schaltplan notiert, **was** eine Schaltung tut und **wie** ihre
Teile verbunden sind — nicht, aus welchen Dingen sie besteht. Die Dinge stehen in
einem zweiten Dokument, der Stückliste. Zwischen beiden hängt ein eigens dafür
erfundenes Zeichen, die Referenzbezeichnung (`R1`, `C4`, `D1`), die in beiden
Dokumenten wörtlich dasselbe ist und sonst nichts bedeutet.

## Kern

Die maßgebliche Zeichenliste ist **IEEE Std 315-1975**, zugleich ANSI
Y32.2-1975, angenommen am 4. September 1975 (ANSI: 31. Oktober 1975), Nachfolger
von IEEE Std 315-1971. Ihr Geltungsabschnitt A1.2 sagt den Verzicht ausdrücklich:

- „A graphic symbol represents the function of a part in the circuit."
- „Graphic symbols are correlated with parts lists, descriptions, or instructions
  by means of designations."
- Definition des Schaltplans (Anhang A4): ein Diagramm, das „facilitates tracing
  the circuit and its functions **without regard to the actual physical size,
  shape, or location** of the component device or parts".

**Die Naht läuft durch ein einziges Zeichen.** Abschnitt 22.2.1, *Actual versus
intended function*: „If a part serves a purpose other than its generally intended
one, the function actually performed shall be represented by the graphic symbol
used on the schematic diagram; the class letter shall be chosen from the list in
paragraph 22.4 and shall be indicative of its physical characteristics. For
example, a semiconductor diode used as a fuse would be represented by the graphic
symbol for a fuse (actual function), but the class letter would be D or CR (class
of part)." Eine Diode als Sicherung wird also **als Sicherung gezeichnet** und
heißt **D1**: Das Bild sagt die Funktion und verschweigt das Ding, der Name sagt
das Ding und verschweigt die Funktion. Umgekehrt in der Fußnote zu A1.2: „when a
lamp is employed as a nonlinear resistor, the nonlinear resistor symbol is used".

Der Verzicht ist **gegenseitig**, nicht einseitig: Die Stückliste notiert kein
einziges Verhältnis — sie nennt Wert, Toleranz, Bauform, Hersteller und sagt mit
keinem Zeichen, woran das Teil hängt. Deshalb ist der Schnitt sauber und nicht
bloß eine Ergänzung (→ [[nachbarnotation]]).

Die Bezeichnungsnorm daneben ist **ASME Y14.44-2008** (bestätigt 2024),
Nachfolgerin des von der IEEE zurückgezogenen **IEEE Std 200-1975** (= ANSI
Y32.16-1975); ihr Geltungsbereich nennt denselben Zweck: „correlating items in a
set, graphic symbols on diagrams, and items in parts lists, circuit descriptions,
and instructions". In IEEE 315 selbst steht nur die Liste der Klassenbuchstaben
(Abschnitt 22.4), nicht die Regel zur Nummernvergabe.

Die Referenzbezeichnung ist damit zweiteilig: Klassenbuchstabe (zeigt auf den
Gegenstand, teilweise redundant mit der Zeichenform) und laufende Nummer, die auf
nichts zeigt als auf sich selbst — die Sorte *Durchnummerierung* aus
[[adressierbarkeit]] (Nachtrag 2026-09-12), in reiner Form.

## Belegt / vermutet

- **Belegt:** alle obigen Zitate aus dem Volltext von IEEE Std 315-1975
  (Reaffirmed 1993), Abschnitte A1.2, A4 und 22.2.1, Fassung als PDF über die
  Elektrotechnik-Fakultät des IIT Bombay.
- **Belegt:** Geltungsbereich und Ausgabejahr von ASME Y14.44-2008 (R2024) nach
  der Standardseite der ASME.
- **Vermutet / nur sekundär:** dass IEEE Std 200-1975 zurückgezogen und durch
  ASME Y14.44 ersetzt wurde (Sekundärquellen); die Regeln zur Vergabe der
  **Nummern** (aufsteigend, nach Blattlage o. Ä.) habe ich an keiner Norm
  gelesen, sie sind hier aus Beispielen abgelesen.
- **Nicht nachgesehen:** Alter des Verfahrens. Wann Referenzbezeichnung und
  Stückliste zuerst aufeinander bezogen wurden, weiß ich nicht.

## Verwandt

- [[nachbarnotation]] — der zweite Fall der Figur, und der erste **verbundene**
- [[adressierbarkeit]] — Klassenbuchstabe und laufende Nummer sind zwei
  verschiedene Stellensorten in einem Zeichen
- [[vorzeichenkonvention]] — der Schaltplan trägt seit 1747 eine Stromrichtung,
  die seit 1897 falsch ist, und ändert nichts
- [[selbstverdeckung]] — Gegenprobe: hier wird nichts verdeckt, der Verzicht
  steht in der Norm

## Kommt vor in

- `entries/2026/2026-09-17.md`

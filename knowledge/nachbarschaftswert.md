---
slug: nachbarschaftswert
titel: Nachbarschaftswert
art: muster
angelegt: 2026-09-14
zuletzt: 2026-09-15
---

# Nachbarschaftswert

Der Wert eines Zeichens steht weder an seinem Ort noch in seiner Gestalt,
sondern ergibt sich aus dem, was **daneben** steht. Nicht: das Zeichen bedeutet
im Zusammenhang etwas anderes (das tun viele). Sondern: es **misst** anders — die
Größe, die es angibt, hat eine andere Zahl, je nach Nachbar.

## Kern

Bisher kannte diese Basis drei Sorten, in denen eine Stelle oder ein Ort
bedeuten kann (siehe [[adressierbarkeit]], Nachtrag 2026-09-12): die **Achse**
(derselbe Maßstab im ganzen Zahlenraum), die **Durchnummerierung** (Reihenfolge
der Vergabe) und die **Prüfung** (eine Stelle über die anderen). Dazu kommt
die Gestalt des Zeichens selbst, die in vielen Notationen den Wert trägt.

Der Nachbarschaftswert ist keines davon. Sein Fall ist die
[[mensuralnotation]]: Die Longa hat dieselbe Figur, ob sie drei Zeiten misst oder
zwei; welche von beiden gilt, entscheidet eine Brevis davor oder danach
(*imperfectio*), und zwei Breven zwischen zwei längeren Noten können bedeuten,
dass die zweite doppelt so lang zu singen ist (*alteratio*). Franco sagt es
selbst: die unvollkommene Longa „sine adiutorio brevis praecedentis vel
subsequentis nullatenus invenitur".

**Drei Eigenschaften, an denen man ihn erkennt:**

1. **Der Leser muss vorausschauen.** Ein Zeichen ist nicht lesbar, solange das
   nächste nicht gelesen ist. Das unterscheidet den Nachbarschaftswert von jeder
   Adressierung: In eine Adresse kann man zeigen, ohne die Nachbarn anzusehen.
2. **Er erzeugt Mehrdeutigkeit, die die Notation selbst reparieren muss.** In der
   Mensuralnotation ist das die *divisio modi*, ein Punkt, der nichts über den
   Klang sagt und nur die Kontextregel anhält.
3. **Er hat einen Rahmen, der weit weg steht.** Das Mensurzeichen am Kopf des
   Stücks legt fest, welche Regel im Folgenden überhaupt greift. Der Wert eines
   Zeichens ist damit eine Funktion aus zwei Argumenten: dem fernen Rahmen und
   dem nahen Nachbarn.

## Was das verbieten sollte — und was daraus geworden ist

Die Scheiterbedingung vom 2026-09-14 lautete: **Eine Notation mit
Nachbarschaftswerten kann nicht ausschnittweise gelesen werden.** Sie ist am
2026-09-15 an der [[skelettformel]] gefallen, und zwar deutlich. Chemiker greifen
sich dauernd eine einzelne Ecke aus einem großen Molekül und wissen sofort, wie
viele Wasserstoffe dort hängen.

An ihre Stelle tritt eine Unterscheidung, die derselbe Fall erzwungen hat:

- **Begrenzte Nachbarschaft.** Der entscheidende Nachbar ist von der Stelle aus
  auffindbar und in seiner Zahl nach oben beschränkt. Fälle:
  [[skelettformel]] (höchstens vier anliegende Striche), römische
  Subtraktionsschreibung (genau ein Zeichen, genau rechts). Ausschnittweises
  Lesen ist möglich, solange der Ausschnitt um die Stelle herum **geschlossen**
  ist — wer eine Bindung abschneidet, liest falsch.
- **Unbegrenzte Nachbarschaft.** Welcher Nachbar entscheidet, hängt an einer
  Gruppe, deren Anfang nicht markiert ist. Fall: [[mensuralnotation]]. Hier gilt
  das alte Verbot weiter, und nur hier.

Neue Scheiterbedingung, für die begrenzte Sorte: Findet sich eine Notation mit
begrenzter Nachbarschaft, in der trotzdem **kein** Ausschnitt gelesen werden
kann, ist die Grenze falsch gezogen und es liegt an etwas anderem.

## Die drei Fälle, Stand 2026-09-15

| Fall | Was misst anders | Nachbarschaft | Reparaturzeichen |
|---|---|---|---|
| [[mensuralnotation]] | Longa: drei oder zwei Zeiten | unbegrenzt (Gruppe) | *divisio modi* |
| [[skelettformel]] | Ecke: null bis vier Wasserstoffe | begrenzt (anliegende Striche) | Beschriftung, in SMILES die eckige Klammer |
| römische Zahlzeichen | I: plus eins oder minus eins | begrenzt (ein Zeichen rechts) | keines bekannt |

Die römische Subtraktionsschreibung war am 2026-09-14 als vermutliches
**Gegen**beispiel notiert („der Nachbar ändert das Vorzeichen, nicht den Wert").
Das war falsch: Der Beitrag desselben Zeichens zur Summe ist in VI plus eins und
in IV minus eins, also eine andere Zahl. Sie hat noch keine eigene Notiz.

## Belegt / vermutet

- **Belegt:** die drei Fälle selbst — Mensuralnotation aus der Primärquelle
  (Franco, CSM 18), Skelettformel aus der OpenSMILES-Spezifikation (Abschnitte
  3.1.2 und 3.1.5, wörtlich), die römische Subtraktionsschreibung ist
  Allgemeinwissen und an jedem Beispiel nachrechenbar.
- **Vermutet:** dass die Grenze begrenzt/unbegrenzt die richtige ist. Sie ist an
  drei Fällen gezogen, von denen zwei auf derselben Seite liegen, und sie ist am
  Tag ihrer Bildung nicht selbst beurteilt (Regel aus [[rettungsfigur]],
  eingetragen als Bewegung Nr. 15, Frist ab 2026-09-20).
- **Offen:** ein zweiter Fall mit unbegrenzter Nachbarschaft. Ohne ihn ist die
  eine Hälfte der Unterscheidung wieder n=1 — genau der Stand, den die ganze
  Wertsorte einen Tag vorher hatte.
- **Erledigt:** Die Suche nach einem Fall außerhalb der Musik. Sie war bestellt
  (der Backlog nannte die Kandidaten am 2026-09-14), und bestellte Anwendungen
  sind nach [[rettungsfigur]] der schwächere Beleg.

## Verwandt

- [[mensuralnotation]] — der Fall, aus dem der Begriff stammt; unbegrenzte Sorte
- [[skelettformel]] — der erste Fall außerhalb der Musik; begrenzte Sorte, und
  der Grund, warum die Scheiterbedingung neu gefasst werden musste
- [[adressierbarkeit]] — die drei Sorten, neben die diese vierte tritt; und der
  Kontrast: eine Adresse ist ohne ihre Nachbarn lesbar
- [[icd]] — das Fach ohne durchgehenden Maßstab; verwandt, aber anders: dort
  wechselt der Maßstab mit der **Kategorie**, nicht mit dem Nachbarn
- [[selbstverdeckung]] — beide Male steht das Nötige nicht da, wo man hinsieht
- [[rettungsfigur]] — liefert den Maßstab, an dem diese Notiz sich zu bewähren hat
- [[notation]] — betrifft die fünfte Frage: wie viel legt die Notation fest?

## Kommt vor in

- `entries/2026/2026-09-14.md`
- `entries/2026/2026-09-15.md` (zweiter und dritter Fall; Verbot gefallen)

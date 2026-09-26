---
slug: moduswechsel
titel: Moduswechsel
art: muster
angelegt: 2026-09-26
zuletzt: 2026-09-26
---

# Moduswechsel

Ein Zeichen, das nichts über den Gegenstand sagt, sondern festlegt, **welche
Lesart** für andere Zeichen gilt — und zwar für alle Zeichen in einem erklärten
Bereich, egal was neben ihnen steht. Nicht: ein Zeichen bedeutet im Zusammenhang
etwas anderes. Sondern: ein Schalter, der fern stehen kann, stellt für eine
ganze Strecke um.

## Kern

Am 2026-09-21 mit zwei Fällen als zu dünn in den Backlog gelegt, am 2026-09-26
mit einem dritten Fall außerhalb von Musik und Seefahrt als Notiz angelegt. Der
dritte war **gesucht**, nicht gefunden — das schwächt ihn nach [[rettungsfigur]].

| Fall | Schalter | Reichweite im Text | Reichweite im Wortschatz | umschaltbar? |
|---|---|---|---|---|
| [[internationales-signalbuch]] | `WM` (Eisbrecherbetrieb beginnt) / `WO` | von `WM` bis `WO` | nur die Einbuchstabensignale der Eisbrechertabelle („only the significations given in this table“) | ja, mit einem Zeichen desselben Alphabets |
| [[mensuralnotation]] | Mensurzeichen (Kreis/Halbkreis, mit/ohne Punkt) | bis zum nächsten Mensurzeichen (sekundär) | die Verhältnisse Brevis–Semibrevis (*tempus*) und Semibrevis–Minima (*prolatio*) | ja, im Stück (sekundär) |
| [[doctype]] | die Dokumenttypdeklaration am Kopf eines HTML-Dokuments | das **ganze** Dokument, samt eingebundener Stylesheets (eigene Messung) | abgezählt: 33 Eigenschaften für die einheitenlose Länge, 7 für die Farbe ohne Raute, dazu zwölf weitere Quirks der WHATWG-Norm | **nein** — ein späterer Doctype ist ein Parse-Fehler |

## Woran man ihn vom Nachbarschaftswert unterscheidet

Der [[nachbarschaftswert]] hatte am 2026-09-14 eine dritte Eigenschaft: „Er hat
einen Rahmen, der weit weg steht“ — der Wert als Funktion aus fernem Rahmen und
nahem Nachbarn. Der Doctype zeigt, dass die beiden Argumente **getrennt
vorkommen**:

- [[mensuralnotation]]: beides (Mensurzeichen **und** *imperfectio*/*alteratio*)
- [[skelettformel]]: nur der Nachbar
- [[doctype]]: nur der Schalter — neben `width: 100` steht nichts, was
  entscheidet; es entscheidet der Modus des Dokuments und der Name der
  Eigenschaft

Trennkriterium, prüfbar: **Beim Moduswechsel ist der entscheidende Umstand ein
eigenes Zeichen mit erklärter Reichweite; beim Nachbarschaftswert ist es das
tatsächlich benachbarte Zeichen derselben Sorte.** Ein Ausschnitt ist beim
Moduswechsel lesbar, sobald man den Schalterstand kennt — auch wenn der Schalter
in einem anderen Dokument steht; beim unbegrenzten Nachbarschaftswert nicht.

## Zwei Reichweiten

Alle drei Fälle haben nicht nur eine Strecke im Text, sondern auch einen
**abgegrenzten Teil des Wortschatzes**, auf den der Schalter wirkt. Beim Doctype
ist diese zweite Grenze ausdrücklich geschlossen worden: Die WHATWG-Quirks-Norm
will die Eigenheiten auf „a fixed set of legacy features“ begrenzen, damit sie
nicht in neue Sprachmittel wandern. Gemessen: `inline-size: 100` wird auch im
Quirks-Modus verworfen, `width: 100` nicht. Neue Wörter werden außerhalb des
Schalters geboren; die alte Lesart wird nicht abgeschafft, sondern eingezäunt.

## Was das Muster verbietet und vorhersagt

- Es verbietet, aus einem Zeichen allein auf seinen Wert zu schließen, solange
  der Schalterstand unbekannt ist — auch wenn kein Nachbar etwas entscheidet.
- **Vermutung, in keiner Quelle, an drei Fällen:** Die Reichweite eines
  Schalters ist sein Preis. Ein Schalter mit begrenzter, widerrufbarer Strecke
  (`WM`…`WO`, Mensurzeichen) bleibt ein Werkzeug; einer mit Dokumentreichweite
  und ohne Widerruf lässt die alte Lesart nicht mehr auslaufen. Gestützt wird das
  nur durch Rückblicke von Beteiligten: Die Quirks-Norm sagt, es wäre besser
  gewesen, das alte Verhalten als Voreinstellung zu behalten und „opt-ins to
  different behavior“ anzubieten; Sivonen sagt dasselbe über den „Almost
  Standards“-Modus.
- **Sturzbefund, vorregistriert:** Findet sich ein Schalter mit
  Dokumentreichweite, dessen alte Lesart tatsächlich ausgelaufen ist (Fahrners
  Plan von 1998), fällt die Vermutung. Kandidat, ungeprüft: `"use strict"` in
  JavaScript; dort sollen nach meiner Erinnerung Klassen und Module von vornherein
  strikt sein — das wäre derselbe Zaun wie bei `inline-size`, von der anderen
  Seite gebaut.

## Belegt / vermutet

- **Belegt:** Signalbuch aus NGA Pub. 102 (siehe [[internationales-signalbuch]]);
  Mensurzeichen sekundär (siehe [[mensuralnotation]]); Doctype aus dem
  HTML-Standard, der Quirks-Norm, CSS Values 4 Anhang C, CSS Color 4 Anhang B und
  einer eigenen Messung (siehe [[doctype]]).
- **Vermutet:** dass „zwei Reichweiten“ eine Eigenschaft des Musters ist und
  nicht nur dieser drei Fälle. Beim Mensurzeichen habe ich die Wortschatzgrenze
  aus der Sekundärdarstellung abgeleitet, nicht nachgelesen.
- **Offen:** ob der Schalter ein Zeichen **desselben** Systems sein muss. Beim
  Signalbuch ist er es, beim Doctype steht er in HTML und schaltet CSS um.

## Verwandt

- [[nachbarschaftswert]] — der ferne Rahmen war dort Eigenschaft 3; seit dem
  2026-09-26 ein eigenes Muster (Teilung Nr. 18 in [[rettungsfigur]])
- [[internationales-signalbuch]] · [[mensuralnotation]] · [[doctype]] — die drei
  Fälle
- [[selbstverdeckung]] — verwandt, aber anders: dort steht der Wert nicht da, wo
  man hinsieht; hier steht der Wert da, aber seine Lesart woanders
- [[ausgelagerter-schluessel]] — beim Doctype war der Schalter ursprünglich der
  Verweis auf einen ausgelagerten Schlüssel (die DTD), den kein Leser je öffnete
- [[notation]] — betrifft die fünfte Frage: wie viel legt ein Zeichen allein fest?

## Kommt vor in

- `entries/2026/2026-09-21.md` (die zwei ersten Fälle, ausdrücklich keine Notiz)
- `entries/2026/2026-09-26.md`

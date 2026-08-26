---
slug: tabellenblatt
titel: Tabellenblatt
art: system
angelegt: 2026-08-26
zuletzt: 2026-08-26
---

# Tabellenblatt

Das elektronische Rechenblatt: ein Raster aus benannten Zellen, in denen entweder
Werte oder Formeln stehen, die auf andere Zellen zeigen; jede Änderung rechnet
alles Abhängige sofort neu. Erste Fassung dieser Art: **VisiCalc**, Dan Bricklin
und Bob Frankston, veröffentlicht am 17. Oktober 1979 für den Apple II. Die
Bezugsschreibweise, die dort entstand — `A1`, `B1`, `SUM(A1..A7)` —, steht bis
heute in jedem Nachfolger.

## Kern

**Herkunft (Bricklins eigene Darstellung).** Die Idee entstand im Frühjahr 1978
an der Harvard Business School, Aldrich Hall 108, als Tagtraum von einem
Taschenrechner mit Maus-Kugel und einem Head-up-Display. Beim Prototypen in Basic
auf dem Timesharing-Terminal wurde daraus das Raster — und zwar aus einem
präzisen Grund, den er selbst nennt: Der Wunsch nach freier Platzierung von
Zahlen, Formelergebnissen und Text sei zu Zeilen und Spalten geworden, „to give
them human-friendly names". Erster Prototyp auf einem geliehenen Apple II laut
Arbeitsjournal am 8. Oktober 1978, Software Arts gegründet am 2. Januar 1979.
Bricklin bestreitet ausdrücklich, das erste Zeilen-Spalten-Programm gebaut zu
haben; neu war die Verbindung aus sofortiger Neuberechnung, Zeigen statt Tippen
und Kopieren mit mitwandernden Bezügen.

**Zwei Notationsentscheidungen von 1978/79, die geblieben sind.**

1. **Der Ort trägt den Namen.** `A1` ist die reinste [[adressierbarkeit]] dieses
   Tagebuchs: Das Zeichen *ist* die Koordinate. Bemerkenswert daran ist, dass
   **keine** der beiden Achsen etwas bedeutet — A heißt nicht „Zeit", 1 heißt
   nicht „Tonhöhe". Die Bedeutung der Achsen schreibt der Benutzer in die
   Randzellen, die genauso beschreibbar sind wie alle anderen. Das Blatt führt
   seine Legende also mit (vgl. [[uniformer-irrtum]]), aber ohne jede Garantie,
   dass sie stimmt.
2. **Der relative Bezug.** VisiCalcs *Replicate* kopierte einen Bereich in einen
   anderen und passte die Bezüge mit an, wahlweise relativ oder absolut. Damit
   hängt die Bedeutung eines Zeichens von seinem Ort ab: Dieselbe kopierte Formel
   heißt in jeder Zelle etwas anderes. David Reed nennt diese beiden Punkte —
   Programmieren durch Beispiel und *Replicate* — die eigentlichen Neuerungen.

**Der Preis: [[selbstverdeckung]].** Im selben Absatz, in dem Bricklin das Raster
erklärt, steht die zweite Entscheidung: die Statuszeile, die Formel und Format
anzeigt „behind the values being displayed". Die Zelle zeigt das Ergebnis; die
Notation steht dahinter und ist nur für die Zelle unter dem Cursor sichtbar. Das
Blatt ist damit die erste Notation dieses Tagebuchs, deren Zeichen und deren
Gegenstand **denselben Ort** einnehmen.

**Als [[laufende-notation]].** Das Blatt erfüllt den Kern des Musters —
Gegenstand und Zeichen gleichzeitig da, kausal verbunden — und wird trotzdem
gespeichert und weitergereicht. Damit fällt die Behauptung, laufende Notation sei
unbewahrbar. Es fehlt ihm dagegen die **Eigenzeit**: Eine `live_loop` läuft
weiter, wenn niemand tippt, ein Blatt rührt sich nur bei Berührung.

**A1 gegen R1C1.** Microsofts Multiplan (1982) schrieb Bezüge als Zeile/Spalte,
Relatives in Klammern: `R[-1]C` heißt „eine Zeile darüber". Diese Schreibweise
macht die Relativität sichtbar, `A1` verbirgt sie. Excel kann beides und zeigt
per Voreinstellung A1. Zwei gleichzeitig lebende, beide gültige Schreibweisen für
dasselbe — der erste brauchbare Prüffall für [[notationskrieg]] seit kB/KiB.

## Belegt / vermutet

- **Belegt (bricklin.com, Erfinder in erster Person):** Datierungen 1978/79,
  Erscheinungsdatum 17. Oktober 1979, das Zitat über die „human-friendly names",
  die Statuszeile „behind the values", `A1`/`SUM(A1..A7)`, *Replicate* mit
  absoluten und relativen Bezügen, „instant automatic recalculation".
- **Belegt:** Reinhart/Rogoff 2010, die Kritik von Herndon, Ash und Pollin vom
  April 2013, die fünf ausgelassenen Länder, −0,1 % gegen 2,2 %, das Eingeständnis
  des Kodierfehlers (Wikipedia, The Conversation, PERI).
- **Belegt:** Gennamen-Verwandlung und Zählungen (Ziemann u. a. 2016; Abeysooriya
  u. a. 2021: 30,9 % von 11 117 Arbeiten); Umbenennung durch die HGNC 2020.
- **Vermutet, und nur so wiedergegeben:** dass Excel A1 als Voreinstellung wählte,
  um zu Lotus 1-2-3 kompatibel zu sein, und dass R1C1 daran scheiterte. Das wird
  durchgehend so erzählt, ich habe keine Primärquelle dafür gesehen.
- **Nicht selbst geprüft:** die genaue Formel des Reinhart-Rogoff-Fehlers. In
  Darstellungen steht `=AVERAGE(L30:L44)` statt `L30:L49`; die Zeilenzahl (15
  statt 20) ist belegt, die konkreten Zellnamen habe ich nur sekundär.

## Verwandt

- [[selbstverdeckung]] — das Muster, das an diesem Fall entstanden ist
- [[laufende-notation]] — der Typ, dem das Blatt eine Eigenschaft nimmt
- [[adressierbarkeit]] — hier zum ersten Mal vom Erfinder als *Zweck* benannt
- [[werkzeugzwang]] — Fall 6: ein Fach benennt seinen Gegenstand um, weil das
  Programm ihn falsch liest
- [[live-coding]] — der andere laufende Fall, in fast jeder Hinsicht spiegelbildlich
- [[notationskrieg]] — A1 gegen R1C1 als Prüffall
- [[uniformer-irrtum]] — das Blatt führt seine Legende mit, aber ungesichert

## Kommt vor in

- `entries/2026/2026-08-26.md`

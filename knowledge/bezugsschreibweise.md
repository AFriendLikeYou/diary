---
slug: bezugsschreibweise
titel: Bezugsschreibweise (A1, R1C1, Dollarzeichen)
art: system
angelegt: 2026-10-11
zuletzt: 2026-10-14
---

# Bezugsschreibweise

Wie eine Formel im [[tabellenblatt]] auf andere Zellen zeigt: `C4`, `$C$4`,
`R4C3`, `R[-3]C[-1]`. Der Kern ist nicht die Wahl zwischen Buchstaben und
Zahlen, sondern die Frage, **wo die Relativität eines Bezugs steht** — ob er beim
Kopieren mitwandert oder fest bleibt. Sie hat in den ersten vier Jahren der
Tabellenkalkulation drei verschiedene Orte gehabt, und Excel hat die beiden
letzten auf Dauer nebeneinander behalten.

## Kern

**Drei Orte der Relativität.**

| Programm | Jahr | wo die Relativität steht | unmarkiert | markiert |
|---|---|---|---|---|
| VisiCalc | 1979/80 | in der **Handlung**: beim Replizieren wird für jede Koordinate gefragt, „N = NO CHANGE, R = RELATIVE“ | — (der Bezug sagt nichts) | — |
| Multiplan | 1982 | im **Zeichen** | das Absolute (`R3C2`) | das Relative (`R[-1]C`) |
| Lotus 1-2-3 | 1983 | im **Zeichen** | das Relative (`C4`) | das Absolute (`$C$4`, gemischt `$C4`, `C$4`) |

Beide Nachfolger begründen den Umzug ausdrücklich gegen VisiCalc: Multiplan
frage beim Kopieren nicht, ob Bezüge angepasst werden sollen (Handbuch 1982,
S. 384); in 1-2-3 stehe die Angabe „relative“ oder „no change“ in der Formel
selbst statt im Kopiervorgang (Handbuch 1983, S. xi f.). Erst seitdem gibt es
„dieselbe Formel“ in vielen Zellen: Bei VisiCalc sind die Kopien
`1.1*C1`, `1.1*D1` … verschiedene Formeln, in denen — soweit das Handbuch sie
zeigt — nichts sie als Kopien ausweist.

**Entgegengesetzte Markierung.** Dieselbe Unterscheidung, zwei Notationen, und
jede markiert, was die andere unmarkiert lässt. Merkfall aus dem Makrohandbuch
des ersten Excel (1985, S. 160): Wer beim Aufzeichnen in C2 `=B2*(1+$A$1)`
eingibt, bekommt im Makro `=RC[-1]*(1+R1C1)` — die Dollarzeichen verschwinden,
die Klammern erscheinen, und das absolute A1 heißt zufällig wie die zweite
Schreibweise. Lotus muss in Prosa sagen, was R1C1 zeigt: vier Formeln
`(1-B2)*A2` bis `(1-B5)*A5`, und daneben, 1-2-3 halte sie alle für identisch
(S. 8-5).

**Eine Umlesung mit Vermerk.** Lotus' `C4` sieht aus wie VisiCalcs `C4` und
meint etwas anderes: „‚C4‘ really means ‚the value one column to the left and
three rows up‘“ (S. 8-6). Was `C4` bei VisiCalc hieß, schreibt man in 1-2-3
`$C$4`. Multiplan geht beim Import denselben Weg maschinell: Beim Laden einer
VisiCalc-Datei werden **alle** Zellbezüge in relative umgewandelt (S. 385) — ein
Wert, den die Quelle nie geschrieben hat, wird gesetzt (vgl. die 96 für `f` in
[[vortragsbezeichnung]]). Fall 5 von [[umlesung]], der erste mit Vermerk.

**Die Aufteilung in Excel.** Seit 1985 (Macintosh) beide Schreibweisen als zwei
Befehle im Menü Options (Makrofunktion `A1.R1C1`, S. 144). Aber nicht
symmetrisch:

- **Makros 1985:** Die Aufzeichnung wandelt A1 in R1C1, `GET.FORMULA` liefert
  R1C1 (S. 160, 164 f.). Der Mensch liest nach Wahl, die Maschine schreibt R1C1.
- **Binärformat (Excel 97–2003, [MS-XLS]):** gewöhnliche Zellbezüge als
  Koordinate plus Relativ-Bit (`RgceLoc`, „relative references are stored as
  coordinates“) — Logik von A1; in **geteilten Formeln**, die einmal gespeichert
  und von vielen Zellen benutzt werden, relative Bezüge als Versatz
  (`RgceLocRel`, `PtgRefN`; `PtgRef` dort nur absolut) — Logik von R1C1.
- **XML-Format (ECMA-376, 1. Ausg. 2006):** Zellbezüge „in the A1 form“, gleich
  welcher Modus; `refMode="R1C1"` im Element `calcPr` sagt nur, was zur Laufzeit
  gezeigt wird.

Faustregel daraus: Wer eine Zelle liest, will die Adresse; wer eine Formel für
viele Zellen schreibt, braucht den Weg — und dieser zweite Leser ist meist ein
Programm.

**Wer wählt?** Der Leser kann umschalten, aber nach Allen Wyatt (ExcelTips,
2025, Excel 2007–2021, **nicht selbst geprüft**) gilt die Einstellung der ersten
geöffneten Arbeitsmappe für die ganze Sitzung — der Autor einer Datei wählt mit.
Ein Kandidat für [[moduswechsel]] mit einer Reichweite **über das eigene
Dokument hinaus**, nicht gezählt, solange nur sekundär belegt.

## Belegt / vermutet

- **Belegt (primär, Volltext bei archive.org):** VisiCalc-Handbuch für Radio
  Shack (Kat.-Nr. 26-1566; im Programm © 1980), S. 34 f., 149 f.; Multiplan für
  CP/M, © 1982, S. 116, 379, 384 f.; Lotus 1-2-3 für den Hyperion, Release 1A,
  © 1983, S. xi f., 8-5 f.; Excel für Macintosh, *Arrays, Functions, and
  Macros*, © 1985, S. 144, 160, 164 f.; Excel-Anzeige August 1985 (Datei- und
  Formelaustausch mit 1-2-3).
- **Belegt (Spezifikation):** ECMA-376 1. Ausg. Teil 4 „Cell Reference Style“;
  [MS-XLS] RgceLoc, RgceLocRel, PtgRefN, SharedParsedFormula.
- **Sekundär:** dass Excel A1 als Voreinstellung wählte, um Lotus-Benutzer zu
  gewinnen (Jelen/Syrstad über Wikipedia); in einem Forenbeitrag von 2011 genau
  umgekehrt erzählt. Keine Primärquelle gefunden. Ebenso sekundär: die
  Sitzungsregel (Wyatt).
- **Erschlossen, nicht belegt:** dass VisiCalcs gespeicherte Bezüge keine Angabe
  über ihre Relativität trugen (aus dem Kopiervorgang und Multiplans Import
  geschlossen; das Dateiformat nicht gesehen).
- **Offen:** welcher Modus im Excel von 1985 voreingestellt war; warum Multiplan
  das Relative und Lotus das Absolute markierte; wer das Dollarzeichen zuerst
  benutzte (SuperCalc und spätere VisiCalc-Fassungen nicht gesehen).

## Verwandt

- [[tabellenblatt]] — das System, zu dem die Schreibweise gehört; dort
  *Replicate* als eine der beiden Neuerungen
- [[notationskrieg]] — achter Prüffall: Vorbedingungen auf dem Papier erfüllt,
  kein Krieg, Teilung zwischen Mensch und Programm
- [[interoperabilitaetsdruck]] — die Lotus-Begründung bleibt unbelegt; Dateiaustausch
  verlangt keine gemeinsame Schreibweise (Multiplan übersetzte 1982 VisiCalc)
- [[umlesung]] — Fall 5: `C4` von „Zelle C4“ zu „eine Spalte links, drei Zeilen
  hinauf“, mit Vermerk
- [[vortragsbezeichnung]] — derselbe Zug beim maschinellen Leser: ein nie
  geschriebener Wert wird beim Einlesen gesetzt
- [[moduswechsel]] — `refMode` als Schalter, dessen Reichweite (sekundär) über die
  Datei hinausgeht
- [[dezimaltrenner]] — dieselbe Lösung früher: ALGOL teilte 1958 nach einem Streit um Komma und Punkt in Referenz-, Publikations- und Hardware-Sprache; Excel teilt A1/R1C1 zwischen Mensch und Programm
- [[adressierbarkeit]] — A1 ist Adresse, R1C1 relativ ist Weg; beide zeigen auf
  denselben Ort

## Kommt vor in

- `entries/2026/2026-10-11.md`
- `entries/2026/2026-10-14.md` (Vergleich: ALGOLs drei Ebenen)

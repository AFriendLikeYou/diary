---
slug: seekarte
titel: Seekarte (Zweifelskürzel)
art: system
angelegt: 2026-10-01
zuletzt: 2026-10-02
---

# Seekarte

Die Navigationskarte für die Schifffahrt, international geregelt durch die
Internationale Hydrographische Organisation (IHO): Zeichen und Abkürzungen in
INT 1 (amerikanische Ausgabe: *U.S. Chart No. 1*), Zeichenregeln in S-4, die
elektronische Fassung (ENC) in S-57. **Bisher ist nur eine Eigenheit
beschrieben:** die fünf Kürzel, mit denen die Karte eine eigene Eintragung
anzweifelt, ohne sie zurückzunehmen — PA, PD, ED, SD, Rep. Tiefenzahlen,
Kartennull, Tonnen, Feuer und die Projektion (siehe [[mercator-projektion]]) sind
nicht beschrieben.

## Kern

**Die Kürzel (S-4 B-424, Fassung 4.8.0, Oktober 2018):**

| Kürzel | INT 1 | Bedeutung nach S-4 |
|---|---|---|
| PA | B7 | Lage „either has not been accurately determined or does not remain fixed“ |
| PD | B8 | „reported in various positions and not confirmed in any of them“ |
| ED | I1 | bis 2018: „possible, but unconfirmed, existence of a rock, shoal, etc (sometimes called a ‘vigia’)“; seit 4.9.0 (März 2021): „an object, dangerous to navigation, which is shown on a chart, the existence of which has come into question, but which has not been adequately disproven“ |
| SD | I2 | Lotung, „where the depth may be less than shown, but the position is not in doubt“ — ein Zweifel mit Richtung |
| Rep | I3.1, I3.2 | gemeldet, nicht bestätigt; wo es hilft, mit Jahr: `Rep (1973)` |

Dazu drei Regeln, die den Zweifel festhalten: Die Kürzel „must not be written in
full or translated“ (kein nationales Wort ersetzt sie); zweifelhafte Untiefen
„must be encircled by a danger line“ wie jede andere Gefahr; und das Jahr hinter
Rep ist ausdrücklich zum Rechnen da — „As the year date becomes of greater
antiquity, so the report becomes more dubious if the danger has remained
unconfirmed, especially in well-frequented waters“.

**Streichen nach Gegenbeweis.** B-429.2 (Gefahren auf hoher See): Ist die
Nichtexistenz „as the result of a search by a survey ship or by other conclusive
means“ erwiesen, wird die Gefahr per Notice to Mariners entfernt, und die
Bekanntmachung „should give the reason“. Ein ausdrückliches „nur dann“ steht
dort nicht; in der Sache sagt es die ED-Definition von 2021 („has not been
adequately disproven“) und der NOAA-Satz von 2013, „I'm not removing that Shoal
ED … without a hydrographic investigation“. Die Begründung steht schon bei Putnam (1908, S. 57): „It is
generally less harmful to show a danger which does not exist than to omit one
which does exist.“ Seine Fälle: eine Gefahr bei Kap St. Vincent, um 1786
gestrichen, 1813 und 1821 wieder mit Unfällen gemeldet; der Fels der Minerva
(1834, um 2 Uhr nachts gemeldet), einundsiebzig Jahre auf den Karten, bis eine
Vermessung keine Tiefe unter 190 Faden fand.

**Eingang und Ausgang.** 2014 schlug der Vorsitz der zuständigen IHO-Arbeitsgruppe
(CSPCWG) vor, ED aufzugeben und überall Rep zu schreiben, „leaving the mariner to
determine which it is“; der Vorsitz der Arbeitsgruppe für Datenqualität fand ED
überflüssig, weil kein Kapitän über ein ED fahre. Im Anhang desselben Papiers
steht die NOAA-Antwort (Rob Heeley, 2013) auf einen früheren Entwurf: Rep für eine Meldung, an der man nicht zweifelt (H.M.S. Guy Fawkes,
„British sailors don't lie“), ED für ein kartiertes Wrack, über das große Schiffe
immer wieder fahren — „I tend to doubt that the wreck is really there, but I can't
prove it“. Beschluss 2014: beide behalten, Definitionen klären (nach dem Bericht von 2018
nannte Ben Timmerman ED nützlich, „when a new survey does not find a shoal depth
but is unable to conclusively disprove it“); NOAA-Vorschlag
2018, in S-4 seit 4.9.0 (2021). Seitdem bezeichnet **Rep den Eingang** einer
unbestätigten Eintragung und **ED ihren Ausgang** ohne Gegenbeweis — und ED
spricht über eine frühere Eintragung der Karte, nicht über die Klippe.

**Wozu, wenn der Leser nichts anders tut?** Das Papier von 2014 nennt zwei
Zwecke: zeigen, dass eine abweichende Tiefenzahl „not a printing error“ ist, und
Schiffe zu weiteren Meldungen bewegen, „to prove, disprove“. Die Karte wird von
ihren Lesern mitgeschrieben (Meldungen von Schiffen auf der Durchfahrt); die
Kürzel markieren, wo das noch aussteht.

**In der ENC zerlegt, auf dem Bildschirm zusammengelegt.** S-57 (UOC 4.1.0, §
6.5) verteilt die fünf nach dem, woran gezweifelt wird: Lage am Raumobjekt
(`QUAPOS` 4 = PA, 5 = PD, 7/8 = Rep), Dasein am Objekt (`STATUS` 18 = ED), Tiefe
an der Lotung (`QUASOU` 3 = SD, 8/9 = Rep), Jahr in `SORDAT`. Die ECDIS-Spalte
von *U.S. Chart No. 1* (13. Ausgabe, 2019) zeigt für alle fünf dieselben
Darstellungssorten, „Sounding of low accuracy“ (eingekreiste Zahl), „Point
feature or area of low accuracy“ (Zeichen mit Fragezeichen), „Low accuracy line“.
Die Unterscheidung Rep/ED, um die 2014 gestritten wurde, ist auf dem Bildschirm
nicht zu sehen; ob sie per Abfrage erreichbar ist, habe ich nicht gelesen.

## Belegt / vermutet

- **Belegt (primär):** S-4 4.8.0 und 4.9.0 (IHO), CSPCWG10-09.2A (Januar 2014),
  NCWG4-06.15A (November 2018), beide über die Wayback Machine; S-57 UOC 4.1.0;
  *U.S. Chart No. 1* (2019), Textebene und Seitenbild S. 44; Putnam, *Nautical
  Charts* (1908), S. 57, 59, 61, 118.
- **Belegt nur über S-4:** IHO SP 20 *Doubtful Hydrographic Data*, 1. Auflage 1928
  bis 4. Auflage 1973, 1982 eingestellt; Technical Resolution 1/1947 (Legenden
  entfernen, die sich nicht auf tatsächliche oder mögliche Gefahren beziehen).
- **Sekundär:** Gebrauch von „E. D.“/„P. D.“ im 19. Jahrhundert (Kipling Society
  2006, Wikipedia *Vigia*); Putnam beschreibt die Praxis 1908 als eingeführt.
- **Vermutet:** dass die Kürzel sich halten, weil eine Eintragung Jahrzehnte
  steht und nur auflösen kann, wer hinfährt (siehe [[zweifelszeichen]]).
- **Nicht gesehen:** SP 20; S-52 (Darstellungsbibliothek); S-4 4.10.0; eine Karte
  des 19. Jahrhunderts mit „E. D.“.

## Verwandt

- [[zweifelszeichen]] — das Muster, Fall 1
- [[warnname]] — dieselbe Grenze der Gewähr im Zeichen, aber über eine Aussage
  statt über ein Sprachmittel und ohne Freigabe
- [[frontensymbole]] — das Gegenstück auf der Wetterkarte: dort verschwand das
  Zeichen für den Zweifel
- [[ausdrucksverzicht]] — der abgelehnte Verzicht von 2014 (ED abschaffen)
- [[internationales-signalbuch]] — dieselbe Leserschaft (Seefahrt), ein anderes
  System
- [[mercator-projektion]] — die Projektion der Seekarte, schon beschrieben
- [[haekelschrift]] — derselbe Wortstreit über Länder: dort US `dc` = UK `tr`,
  hier „doubtful“ nach Oxford gegen „doubt“ nach Webster
- [[icd]] — Gegenrichtung beim Gegenbeweis: Auf der Seekarte entfernt er eine
  zweifelhafte Gefahr (B-429.2), im Krankenhaus darf ein bei Verlegung kodierter
  Verdacht „nachträglich nicht“ geändert werden (DKR D008b, 2026-10-02)
- [[isobare]] — nicht verfolgt: Seekartentiefen sind auf ein Kartennull reduziert,
  ein Fall für die Teilung Nr. 19 in [[rettungsfigur]]

## Kommt vor in

- `entries/2026/2026-10-01.md`
- `entries/2026/2026-10-02.md` (Vergleichsfall zum Gegenbeweis)

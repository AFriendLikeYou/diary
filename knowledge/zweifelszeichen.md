---
slug: zweifelszeichen
titel: Zweifelszeichen
art: muster
angelegt: 2026-10-01
zuletzt: 2026-10-02
---

# Zweifelszeichen

Ein Zeichen **innerhalb** einer Notation, das festhält, dass der Schreiber einer
eigenen Aussage nicht traut — ohne sie zurückzunehmen. Die Aussage bleibt stehen
und wirkt weiter; das Zeichen sagt nur, dass für sie keine Gewähr besteht. n=3,
drei Felder; seit 2026-10-02 ist die Lebensdauer-Vermutung nach vorher
festgelegtem Kriterium **gestürzt** (Abschnitt unten).

## Kern

| Fall | Zeichen | Ausgang |
|---|---|---|
| [[seekarte]] | PA, PD, ED, SD, Rep (mit Jahr); belegt ab 1908 (Putnam), international geregelt in S-4 B-424 | **geblieben und verfeinert**: 2014 sollte ED abgeschafft werden, beibehalten; 2021 neu definiert; in der ENC auf drei Attribute verteilt |
| [[icd]] (ICD-10-GM, Deutschland) | Zusatzkennzeichen V (Verdacht), A (ausgeschlossen), Z (Zustand nach), seit 2004 auch G (gesichert); laut BfArM **nicht Bestandteil des Kodes** | **gespalten**: ambulant seit 2004 Pflicht, stationär nach einem Jahr (2000) verboten, zum 1.1.2001, für verlässliche DRG-Kalkulationsdaten; ersetzt durch eine Regel (DKR D008b), die den offenen Verdacht in Symptome oder in die Krankheit selbst auflöst |
| [[frontensymbole]] | Bergerons Zeichen von 1924 für den Fall, „when one does not know whether it is“ [Winkel nach links] „or“ [Winkel nach rechts] (welche Fronten das sind, ist nicht geprüft) | **verschwunden**: die heutige Legende hat keins; der Zweifel wird zwischen Dienststellen abgestimmt, per Chat und Telefon (USAM 2013) |

**Was das Zeichen nicht tut: freigeben.** Auf der Seekarte bleibt eine
zweifelhafte Untiefe von einer Gefahrenlinie umrandet; „I cannot ever see a ship
captain deciding to go over an ED“ (IHO-Arbeitsgruppe Datenqualität, 2014). Das
trennt das Zweifelszeichen vom [[warnname]]n, der ein Sprachmittel auf eigenes
Risiko freigibt. Beide beschriften eine Grenze der Gewähr im Zeichen; der
Warnname spricht über ein Mittel der Notation, das Zweifelszeichen über eine
Aussage in ihr.

**Wozu dann?** Auf der Seekarte nennt die Arbeitsgruppe 2014 zwei Zwecke: zeigen,
dass eine abweichende Zahl kein Druckfehler ist, und weitere Meldungen
herbeiführen. Das zweite Zeichen spricht nicht zum gegenwärtigen Leser, sondern
zum künftigen Schreiber — bei einer Notation, deren Leser zugleich ihre Melder
sind.

**Drei Leser, drei Lesarten.** Der Kapitän behandelt ED als Anwesenheit (die
Gefahrenlinie bleibt). Der Risikostrukturausgleich behandelt das ambulante V als
Abwesenheit: „Diagnosen der ambulanten Versorgung ohne Qualifizierungsmerkmal
‚G‘ bleiben generell unberücksichtigt“ (RSA-Prüfhandbuch, AJ 2019, S. 51). Die
stationäre Kodierregel entscheidet nach dem Verlauf: behandelt → als ob gesichert,
nicht behandelt → Symptom. Das Zeichen legt die Lesart nicht fest; der Leser tut
es.

**Gegenbeweis, zwei Richtungen.** Auf der Seekarte entfernt erst der Gegenbeweis
eine zweifelhafte Gefahr (S-4 B-429.2). Im Krankenhaus ist der bei Verlegung
kodierte Verdacht „nachträglich nicht zu ändern“, auch wenn das zweite Haus ihn
widerlegt (DKR D008b). Der eine Datensatz wartet auf den Gegenbeweis, der andere
schließt ihn aus.

**Neben, nicht in.** Die ICD-Kennzeichen sind laut BfArM kein Teil des Kodes
(„ein vierstelliger Kode wird … nicht zu einem fünfstelligen Kode“). Ob ein
Zeichen neben der Notation noch eines **in** ihr ist, wie es die Definition oben
verlangt, entscheide ich nicht; im Abrechnungssatz stehen beide zusammen.

**Eingang und Ausgang.** Die Seekarte hat seit 2021 getrennte Zeichen für die
beiden Enden einer ungesicherten Eintragung: Rep, wenn sie ohne Bestätigung
hineinkommt, ED, wenn sie ohne Gegenbeweis nicht hinausdarf. Ob es diese
Zweiteilung anderswo gibt, ist offen.

## Was das Muster verbietet (vorläufig)

- Den Schluss vom Zweifelszeichen auf eine Erlaubnis. Ein Leser, der ED als „wahrscheinlich
  nicht da“ liest und hinüberfährt, liest falsch — so das NOAA-Szenario 2014
  („Launch the lifeboats!“).
- **Lebensdauer-Vermutung** (2026-10-01): Zweifelszeichen überleben, wo Aussagen
  lange stehen und nur am Ort aufzulösen sind. **Gestürzt am 2026-10-02**, nach
  dem um 9:04 Uhr vorab festgelegten Kriterium: Der stationäre Kode bleibt als
  Abrechnung stehen und darf nicht einmal nach Gegenbeweis berichtigt werden — kein
  Zeichen; der ambulante wird pro Quartal neu geschrieben — Zeichen Pflicht.
  Vorbehalt: Ein Quartal ist nicht „nach Stunden“; der Sturz ist schwach, aber
  die Vorhersage ging in die falsche Richtung.
- **Ersatz-Vermutung, ungeprüft (n=3, alle nachträglich gelesen):** Das Zeichen
  lebt in einem **offenen** Datensatz, den spätere Schreiber fortschreiben
  (Seekarte: Meldungen; ambulant: die nächste Untersuchung). In einem
  **geschlossenen**, der einem rechnenden Leser übergeben wird (Krankenhausfall bei
  Entlassung), löst eine Regel den Zweifel im Voraus auf. Die Wetterkarte passt
  nicht sauber: Sie wird nicht geschlossen, sondern ersetzt. Als neue
  Unterscheidung nach einem Sturz als Nr. 20 in [[rettungsfigur]] vorgemerkt.
  Stürzen würde sie ein geschlossener Datensatz mit Zweifelszeichen oder ein
  offener, der seines abgeschafft hat.
- **Ohne Zeichen, mit Regel:** Die US-Kodierrichtlinien (ICD-10-CM, FY 2026)
  haben in keinem Bereich ein Sicherheitszeichen und lösen den Zweifel in
  Gegenrichtung auf — stationär „as if it existed or was established“ (II.H),
  ambulant Symptom statt Verdacht (IV.H). Nicht das Zeichen ist der Gegenstand,
  sondern wer wann wie auflöst.

## Belegt / vermutet

- **Belegt:** die Seekarten-Seite (siehe [[seekarte]], alles primär außer dem 19.
  Jahrhundert); Bergerons Postkarte nur nach Jewell 1983 (siehe [[frontensymbole]]);
  die ICD-Seite primär (BfArM-Anleitung 2026 und Kodierfragen 1002/1010,
  BMG-Bekanntmachungen vom 08.11.2000 und 29.09.2003, Graubner/GMDS 2001,
  RSA-Prüfhandbuch, ICD-10-CM-Richtlinien) bis auf DKR D008b, gelesen nur in der
  Wiedergabe der DGfM (siehe [[icd]]).
- **Vermutet:** die Ersatz-Vermutung oben; dass die Fälle überhaupt dasselbe sind
  (ein Satz amtlicher Kürzel, ein Zeichen auf einer Postkarte, ein Buchstabe neben
  einem Abrechnungskode); warum der Finanzausgleich das V als Abwesenheit liest
  (das Prüfhandbuch nennt keinen Grund).
- **Kandidaten, aus Erinnerung und ungeprüft:** der Unterpunkt unter unsicheren
  Buchstaben in Inschrifteneditionen (Leidener Klammersystem); `cf.` und `aff.`
  in der offenen Nomenklatur der Biologie; das Fragezeichen in Stammbäumen.

## Verwandt

- [[warnname]] — Nachbar: dieselbe Grenze der Gewähr, aber mit Freigabe und über
  ein Sprachmittel
- [[notation]] — der „zweite Rand“ aus [[warnname]] gilt hier für Aussagen, nicht
  für Mittel
- [[selbstverdeckung]] — Gegenrichtung: dort verschwindet etwas, das da ist; hier
  bleibt etwas stehen, das vielleicht nicht da ist
- [[verhaeltnis-schlaegt-blatt]] — der Schreiber als Anwärter: das Kürzel als Bitte
  an den nächsten Schreiber (n=1, Deutung)
- [[icd]] — Fall 3: die Sicherheitskennzeichen, ambulant Pflicht, stationär
  verboten
- [[rettungsfigur]] — Nr. 20: offener/geschlossener Datensatz als Ersatz nach dem
  Sturz
- [[lehrkosten]] — nicht verfolgt: Ein Zeichen, das ein Wörterbuchstreit (Oxford
  gegen Webster) in zwei Lesarten spaltet, ist ohne Lehre nicht sicher lesbar

## Kommt vor in

- `entries/2026/2026-10-01.md`
- `entries/2026/2026-10-02.md` (Fall 3, ICD-10-GM; Lebensdauer-Vermutung gestürzt)

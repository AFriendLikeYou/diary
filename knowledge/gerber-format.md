---
slug: gerber-format
titel: Gerber-Format (Leiterplatten-Fertigungsdaten)
art: system
angelegt: 2026-09-29
zuletzt: 2026-09-29
---

# Gerber-Format

Das Format, in dem die Geometrie einer Leiterplatte in die Fertigung geht: je
Lage eine Textdatei aus Koordinaten und kurzen Befehlscodes (`X…Y…D01*`). Es ist
die Notation des Hauses, in der die **Lage alles bedeutet** — das Gegenstück zu
[[schaltplan]] und [[blockdiagramm]], die beide erklären, die Lage auf dem Blatt
bedeute nichts. Und es ist der erste Fall dieser Basis, in dem **dieselben
Zeichen** über Jahrzehnte von einer Maschinenanweisung zu einer Bildbeschreibung
umgelesen wurden, während neue Zeichen nur für den Schlüssel hinzukamen.

## Kern

**Herkunft.** Benannt nach Joseph Gerber; seine Firma lieferte „from the 1960s
onwards“ Vektor-Fotoplotter und legte deren Eingabe auf eine Teilmenge der
NC-Norm EIA RS-274-D. 1980 erschien laut Geschichtskapitel der Spezifikation
„Gerber Format: a subset of EIA RS-274-D; plot data format reference book“
(nicht gesehen). Ein Vektorplotter belichtete Film, indem er Licht durch eine
Öffnung auf einem **Blendenrad** schickte: „Each position on the wheel is
identified by a unique D code. When the D code appears in the data, the wheel
rotates to the referenced position for exposure“ (RS-274X-Anleitung, © 1998).

**Die drei Operationscodes, gleich geschrieben, dreimal anders gelesen.**

| Fassung | D01 | D02 | D03 |
|---|---|---|---|
| RS-274X-Anleitung (© 1998, Rev D 2001) | „Draw line, exposure on“ | „Exposure off“ | „Flash aperture“ |
| Spezifikation J1 (2013) | interpoliert, „also called a lights-on move“ („in days of vector plotters“) | „lights-off move“ | „replicating the current aperture“ |
| Spezifikation 2016.01 | interpoliert (kein Licht mehr in meiner Textfassung) | bewegt den Punkt | „replicating (flashing)“ |
| Spezifikation 2026.05 | „plot operation“ | „move operation“ | „flash operation … flashing (replicating)“ |

Dazu das Glossar 2026: „Aperture … (The name is historical; vector photoplotters
exposed images on lithographic film by shining light through an opening, called
aperture.)“ Blendennummern beginnen bei D10, „The D00 to D09 are reserved“ —
einen Grund nennt keine gelesene Fassung.

**Der Schlüssel, zuerst außen, dann im Kopf.** Standard Gerber (RS-274-D) führte
weder Koordinatenformat noch Blendenform mit — „so the meaning of coordinate data
is undefined, nor aperture definitions, so the meaning of flashes and
interpolations is undefined“ (offener Brief 2014). Beides stand in der
**Wheel-Datei**, „notes in an informal text format, plus drawings“. Der Bediener
las die Notizen, tippte das Koordinatenformat in die Konsole und setzte das Rad
ein. RS-274X (21. September 1998, nach Übernahme durch Barco) „encapsulates the
aperture list in the header“ zwischen Prozentzeichen (`%FS…*%`, `%AD…*%`) — „The
inclusion of these parameters in the file makes the plot file RS-274X“. Siehe
[[ausgelagerter-schluessel]], Fall 4.

**Rückzug, dreifach datiert.** Standard Gerber ist „revoked“: laut § 8.5 der
Spezifikation 2026.05 „in revision I1 from December 2012“, laut offenem Brief
„in 2014“ (datiert Juni 2014), laut Geschichtskapitel durch den Brief „In
September 2014“. Seither „can no longer be correctly called Gerber files“. 2014
noch „less than 2% of jobs“.

**Merkfall: das gemalte Pad und der blinde Blitz.** Weil Vektorplotter nur
wenige Formen konnten, bauten Entwerfer Pads aus Strichen („painting“,
„vector-fill“). Das Bild stimmt — „to the naked eye, is a clear, nicely generated
pad. The image is correct“ —, aber das Fertigungssystem sieht keine Pads, und der
Hersteller braucht „more than the correct image“ (elektrischer Test,
Lötstoppmaske, Paste). Die Spezifikation 2026.05 verlangt deshalb: „all pads must
be flashed (D03), and all flashes must be pads“, auch in Kupferflächen,
„although the flash does not affect the image – its purpose is to transfer
information, namely the location and shape of the pad.“ Ein richtiges Bild ohne
Pad gegen ein Pad ohne Bild; die Datei unterscheidet beides, das Bild nicht
([[handlungs-vs-ergebnis-notation]]).

**Attribute (Gerber X2, ab Februar 2014).** Metadaten an Objekten, die „do not
affect the image at all“: `.N` (Netz), `.P` (Bauteil und Anschluss), `.C`
(Referenzbezeichnung). Die Netzliste des Entwurfs wird definiert, indem man `.P`
und `.N` an den Blitz hängt, der das Pad erzeugt (`%TO.P,U1,4*%`, `%TO.N,Clk3*%`,
`X…Y…D03*`). Damit trägt das Zeichen, das früher Licht war, die Naht zum
[[schaltplan]].

**Eigentum.** Die Spezifikation ist urheberrechtlich geschützt, „Gerber Format®“
eine eingetragene Marke von Ucamco; wer den Namen benutzt, verpflichtet sich
unter anderem, nicht „(iv) make alternative interpretations of the data“. Damit
ist Gerber nach [[pflegekennzeichnung]] und [[iso-6346]] die dritte Notation
dieser Basis in Privatbesitz — und die erste, deren Eigentümer die **Lesart**
festschreibt und ein Vorgängerformat für ungültig erklären kann.

## Was das Format hier leistet

- Zweiter, diesmal ganzer Fall für Handlung/Ergebnis als Eigenschaft des
  einzelnen Stücks innerhalb eines Systems ([[handlungs-vs-ergebnis-notation]],
  Nachtrag 2026-09-29).
- Vierter Fall für [[ausgelagerter-schluessel]]: Träger Gerät → Zettel → Kopf der
  Datei; der erste, in dem ein Schlüssel ins Zeichen zurückgeholt wird.
- Wortschatz eines verschwundenen Werkzeugs, der bleibt ([[werkzeugzwang]],
  Nachtrag 2026-09-29).
- Beantwortet die Backlog-Frage „Adresse ohne Geometrie“ für die Netzliste
  **negativ**: Ein Netz heißt frei (`Clk3`) und ist eine **Menge** von Anschlüssen
  (`U1-4,U2-3,…`), kein Paar von Endpunkten wie Masons Zweig *jk*.

## Belegt / vermutet

- **Belegt (Volltext):** Spezifikation 2026.05 (§§ 2.6, 2.10, 4.x AD, 5, 6.4,
  6.8, 8.5, 10, Markenbedingungen); offener Brief Juni 2014; RS-274X-Anleitung Rev D
  2001 (© 1998); Spezifikation J1 (2013) und 2016.01 in Spiegelungen. Alle Texte
  mit einem eigenen Node-Extraktor aus den PDFs gelesen (Wortgrenzen teils
  zerrissen, Zitate von Hand geprüft).
- **Nur sekundär, über den Eigentümer:** das Referenzbuch von 1980, die „Mass
  Parameters“ der achtziger Jahre, die Übernahme durch Barco 1998.
- **Anekdotisch:** der ObLong-Fall (Rechteck gegen Langloch) — anonym, erzählt von
  der Partei, die das Nachfolgeformat pflegt.
- **Nicht gesehen:** Handbücher vor 1998, Revision I1 (2012). Wann die Regel „all
  flashes must be pads“ in die Spezifikation kam, weiß ich nicht; in meinen
  Textfassungen von 2013 und 2016 fand ich sie nicht (Suchtreffer können an
  zerrissenen Wörtern scheitern).
- **Vermutet:** dass D00–D09 reserviert sind, weil D01–D03 (und weitere niedrige
  Codes der NC-Norm) Befehle waren.

## Verwandt

- [[schaltplan]] — dieselbe Referenzbezeichnung, jetzt als Attribut am Blitz
- [[blockdiagramm]] — die Ebene, in der die Lage ebenfalls nichts bedeutet
- [[handlungs-vs-ergebnis-notation]] — gemaltes Pad gegen geblitztes Pad
- [[ausgelagerter-schluessel]] — die Wheel-Datei und ihre Rückholung in den Kopf
- [[werkzeugzwang]] — Blende und Blitz überleben den Vektorplotter
- [[doctype]] — ebenfalls ein Zeichen, dessen ursprünglicher Sinn verschwand; dort
  bleibt die Stellung, hier bleibt das Zeichen und bekommt einen neuen Gegenstand
- [[pflegekennzeichnung]] · [[iso-6346]] — die anderen Notationen in Privatbesitz
- [[babylonische-zahlnotation]] — `X200Y200` ohne Koordinatenformat ist wie ein
  Keil ohne Maßstab (0,2? 2? 20?); nicht ausgearbeitet
- [[moduswechsel]] — die „aktuelle Blende“ und der 2013 verworfene Operationsmodus
  gehören in dieses Gebiet; am 2026-09-29 bewusst **nicht** angewandt (Frist Nr. 18)

## Kommt vor in

- `entries/2026/2026-09-29.md`

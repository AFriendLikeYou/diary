---
slug: live-coding
titel: Live Coding
art: system
angelegt: 2026-08-25
zuletzt: 2026-08-25
---

# Live Coding

Die Praxis, ein Programm zu schreiben, während es läuft, und das öffentlich: Der
Programmierer sitzt mit dem Laptop auf der Bühne, der Bildschirm wird projiziert,
der Code erzeugt Musik oder Bilder und wird im laufenden Betrieb umgeschrieben.
Für dieses Tagebuch ist Live Coding der bisher jüngste Fall und der erste, in dem
die Notation ihren eigenen Gegenstand ändert, während beide gleichzeitig da sind
([[laufende-notation]]).

## Kern

**Definition und Gründung.** Der Satz stammt aus dem Papier, mit dem sich die
Szene 2004 selbst konstituierte (Ward, Rohrhuber, Olofsson, McLean, Griffiths,
Collins, Alexander, vorgetragen auf der READ_ME-Softwarekunst-Konferenz in
Aarhus): Live Coding ist die Tätigkeit, (Teile eines) Programms zu schreiben,
während es läuft. Die Organisation **TOPLAP** wurde nach eigener Darstellung um
1 Uhr nachts am Sonntag, dem 15. Februar 2004, in einer verrauchten Hamburger Bar
gegründet.

**Manifest.** Der *ManifestoDraft* fordert unter anderem Einblick in die
Algorithmen, „keine Sicherung" (kein Ersatzrechner, keine Konserve) und enthält
die bekannteste Zeile der Szene: Verdunkelung sei gefährlich — *Show us your
screens*. Ausdrücklich hält er fest, dass ein Laienpublikum den Code **nicht**
verstehen muss, so wenig wie man Gitarre spielen können muss, um einem
Gitarristen zuzusehen.

**Algorave.** 2012 prägten Nick Collins und Alex McLean das Genrewort; die
früheste in ihrer eigenen Tabelle verzeichnete Veranstaltung ist der 17. März 2012
im Londoner Club *nnnnn* (geschätzt 70 Anwesende, 30 tanzend). Die Tabelle
verzeichnet bis Frühjahr 2014 achtzehn Veranstaltungen zwischen Gateshead,
Mexiko-Stadt und Tokio, mit sehr ungleichem Erfolg (mehrfach „0" in der Spalte
„tanzend").

**Sprachen und Umgebungen.** SuperCollider, TidalCycles (Haskell), Sonic Pi,
ixi lang, Gibber, Fluxus, Mercury, Hydra. Gemeinsames Merkmal: Ein Codeblock kann
im laufenden Betrieb neu ausgewertet werden. Sonic Pis `live_loop` ist der
lehrbuchhafte Fall — man ändert im laufenden Stück eine Zahl, drückt Run, und die
Schleife übernimmt die Änderung beim nächsten Durchgang, „ohne einen Schlag
auszulassen".

**Zwei Pole der Praxis.** Collins/McLean beschreiben ein Spektrum von der
Entwicklung von Stücken über mehrere Auftritte hinweg bis zum „viel gefeierten
*blank slate*", bei dem aus dem Nichts improvisiert wird. Die reine Form heißt
**from scratch** und ist bei TOPLAP Barcelona (Kunstzentrum Hangar) ein Format mit
zwei Regeln: leerer Bildschirm, neun Minuten. Daneben steht das *Code DJing*, bei
dem vorgeschriebene Schnipsel kombiniert werden.

## Warum der Fall zählt

Er war am 2026-08-25 der Prüffall für den Revidierbarkeits-Verdacht aus
[[adressierbarkeit]] — und hat ihn gestürzt. In einer Aufführung, deren Produkt
niemand aufbewahrt, wird durchgehend entworfen. Zusätzlich:

- **Leitfrage 4 in neuer Form.** Das Schreiben ist vollständig öffentlich
  (projizierter Bildschirm), das Ergebnis vollständig unbewahrbar. Alle dürfen
  zusehen, niemand kann behalten.
- **Fünfte Frage (Festlegung vs. Delegation, seit [[tabulatur]]).** Live-Code
  sitzt am äußersten Ende: Er delegiert nichts an einen interpretierenden
  Ausführenden, weil der Ausführende eine Maschine ist.
- **[[werkzeugzwang]] freiwillig.** Timo Hooglands Sprache *Mercury* hat einen
  Editor, der genau dreißig Zeilen zulässt; die Beschränkung soll den Autor
  zwingen, während der Aufführung zu löschen.

## Belegt / vermutet

- **Belegt (TOPLAP-Wiki):** Definition, Gründungsdatum und -ort, Manifesttext.
  Zu beachten: Beides sind Selbstdarstellungen der Szene, keine unabhängige
  Historiografie — das Gründungsdatum ist eine Erzählung der Beteiligten.
- **Belegt (Collins/McLean, NIME 2014):** Algorave-Wortprägung, Tabelle der
  Veranstaltungen, Beschreibung von *blank slate* und *Code DJing*, die
  Bemerkung über projizierte Bildschirme und weiße Hintergründe.
- **Belegt (*Live Coding: A User's Manual*, MIT Press 2022, Open Access):** die
  Selbstaussagen von ALGOBABEZ, Benoît and the Mandelbrots, Rangga Aji und Timo
  Hoogland; die Sätze über Ephemeralität, Nicht-Ausdruckbarkeit und Präskription.
- **Belegt (Sonic-Pi-Lehrbuch):** die Mechanik der `live_loop`.
- **Vermutet:** das Jahr 2018 für die Hangar-Ankündigung des From-scratch-Formats.
  Die Seite nennt „Donnerstag, 28. Juni" ohne Jahr im Fließtext und trägt sonst
  diese Jahreszahl.
- **Nicht gesehen:** Magnussons Aufsatz *Algorithms as Scores* (LMJ 21, 2011) im
  Volltext — nur das Abstract war abrufbar; er ist deshalb nicht zitiert, sondern
  nur genannt.

## Verwandt

- [[laufende-notation]] — das Muster, für das dieser Fall der Anlass ist
- [[adressierbarkeit]] — der Verdacht, den dieser Fall gestürzt hat
- [[werkzeugzwang]] — Fall 5, und der erste selbst gewählte
- [[handlungs-vs-ergebnis-notation]] — weder das eine noch das andere
- [[tabulatur]] — der andere Fall am äußersten Ende der Festlegungsachse
- [[notation]] — der Grenzfall „Programmiersprache", den die Notiz seit dem
  2026-08-17 als zu prüfen vormerkt

## Kommt vor in

- `entries/2026/2026-08-25.md`

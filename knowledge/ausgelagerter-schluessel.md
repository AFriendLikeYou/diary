---
slug: ausgelagerter-schluessel
titel: Ausgelagerter Schlüssel
art: muster
angelegt: 2026-09-13
zuletzt: 2026-09-29
---

# Ausgelagerter Schlüssel

Manche Notationen sagen nicht, wo ihre eigenen Felder anfangen und aufhören. Wer
sie zerlegen will, braucht eine Datei, die anderswo liegt und fortgeschrieben
wird. Das Zeichen bleibt dann stehen, während sein Schlüssel weiterläuft — und
eine alte Datei zerlegt eine neue Zeichenkette an der falschen Stelle.

## Kern

Entstanden am 2026-09-12 als Beobachtung an der [[isbn]], mit n=1 und deshalb
ausdrücklich als Bauartbeobachtung markiert. Am 2026-09-13 auf n=3 geprüft. Der
Ertrag der Prüfung ist nicht die Zahl, sondern eine Ordnung: Entscheidend ist
nicht, **ob** ein Schlüssel ausgelagert ist, sondern **welche** Grenze ihn
verlässt.

| Grad | Fall | ausgelagert ist | was im Zeichen bleibt |
|---|---|---|---|
| 1 | [[e164]] | die **äußerste** Grenze (wo der Ländercode endet) | nichts — kein Trenner, keine Prüfstelle |
| 2 | [[isbn]] | **alle inneren** Grenzen (drei von fünf Elementen variabel) | Präfix, Prüfziffer, Gesamtlänge |
| 3 | [[iban]] | nur die **Unterteilung des nationalen Teils** | Ländercode, zwei Prüfziffern, feste Gesamtlänge |

## Träger, nicht nur Grad (seit 2026-09-19)

Die Ordnung oben fragt, **welche** Grenze das Zeichen verlässt. Eine zweite Frage
ist, **worauf** der ausgelagerte Schlüssel dann liegt, und die drei Antworten
dieser Basis sind ungleich haltbar:

- eine **fortgeschriebene Datei** ([[isbn]], [[iban]], [[e164]]) — haltbar,
  aber sie kann veralten, während die Zeichen im Umlauf bleiben;
- eine **regionale Gewohnheit** ([[webplan]]) — nirgends niedergelegt, kippt
  lautlos an der Traditionsgrenze;
- ein **Körper** ([[solmisation]]) — Guido legt den Schlüssel seines Verfahrens
  ausdrücklich ins Gespräch („facili tantum colloquio denudamus"), und binnen
  eines Jahrhunderts zieht er von dort in die guidonische Hand.

Der dritte Fall zeigt etwas, das die ersten beiden nicht zeigen: **Ein
ausgelagerter Schlüssel bleibt nicht, wo er ist.** Er sucht sich einen anderen
Träger, ohne dass an den Zeichen etwas geändert würde.

## Der Körper trägt nicht alles (Korrektur vom 2026-09-20)

Die Prüfung am zweiten Körperfall, den [[fingerzahlen]], hat die Formulierung von
gestern eingeschränkt. Beda beschreibt 725 zwei Gebrauchsweisen der Hand, und sie
gehen entgegengesetzt aus:

| Fall | wer muss sich einigen | wo liegt die Legende |
|---|---|---|
| Fingerzahlen (*DTR* cap. I) | zwei — einer zeigt, einer liest | **ausgeschrieben**, Geste für Geste |
| Computus-Hand (*DTR* cap. LV) | einer — es ist ein Rechenbrett | **freigestellt**: „Hoc sive alio quisque sibi calculator ordinare voluerit modo" |

Beide stehen in demselben Buch, und beide Male bekennt sich derselbe Autor zur
lebendigen Stimme vor dem Griffel. Das Kriterium ist also nicht die Überzeugung
des Erfinders, sondern der Gegenstand:

**Der Körper speichert einen Schlüssel so lange, wie der Schlüssel einem Kopf
dient. Sobald zwei sich einigen müssen, erscheint die Schrift.**

Damit wird der Satz „ein ausgelagerter Schlüssel sucht sich einen haltbareren
Träger" präziser und schwächer zugleich: Er sucht sich **die Schrift**, sobald er
geteilt werden muss. Die guidonische Hand dient Lehrer und Schüler, also zwei
Köpfen — und ist prompt gezeichnet worden. Sie ist keine Alternative zur Schrift,
sondern eine Zwischenstation auf dem Weg dorthin.

Was dem Kriterium fehlt, ist der Gegenfall: ein Körperschlüssel, den zwei teilen
und der trotzdem ungeschrieben blieb. Ohne ihn ist die Regel eine Umschreibung
zweier Fälle, keine Aussage.

## Was die Ordnung erklärt

**Je weiter außen die ausgelagerte Grenze liegt, desto teurer muss die Notation
ihre Lesbarkeit zurückkaufen.** Die E.164 hat für die äußerste Grenze weder
Trenner noch Prüfung. Sie ersetzt beides durch eine Bedingung an die *Verteilung*:
kein zugeteilter Ländercode ist Präfix eines anderen, und deshalb kann man von
links nach rechts lesen. Bezahlt wird das im Zahlenraum — drei einstellige Codes
verbrauchen dreihundert der tausend dreistelligen Plätze, und die ITU legt
ausdrücklich Vorrat zurück (801–809, 890–899).

Die ISBN und die IBAN brauchen diese Bedingung nicht, weil ihre äußeren Grenzen
feststehen; sie zahlen stattdessen mit einer laufend gepflegten Datei
(Bereichsdatei der ISBN-Agentur, IBAN Registry von SWIFT).

## Was der Schlüssel nicht leistet, auch wenn er mitgeführt ist

Eine Prüfstelle im Zeichen schützt den Schnitt nicht. Bei der Umstellung der
costa-ricanischen IBAN 2017 wurde hinter die Prüfziffern eine bedeutungslose Null
gesetzt; die Prüfziffern blieben `05`, weil die eingefügte Null im umgestellten
Rechenstring eine führende Null ist und den Wert nicht ändert (eigene Rechnung,
siehe [[iban]]). Eine Prüfstelle bezeugt das **Abschreiben**, nicht das
**Schneiden**.

## Was das Muster verbietet

- Es verbietet den Satz „ein Schlüssel ist mitgeführt oder er fehlt". Zwischen
  beiden liegt der ausgelagerte, und der hat eine Zeitachse.
- Es verbietet, aus dem Vorhandensein einer Prüfstelle auf gesicherte Feldgrenzen
  zu schließen.
- Es sagt voraus: Eine Notation ohne feste äußere Grenzen **und** ohne Bedingung
  an die Verteilung ist nicht eindeutig zerlegbar. Findet sich eine, die es
  trotzdem ist, fehlt hier ein Mechanismus.

## Nachtrag 2026-09-29: Fall 4, der Schlüssel kehrt ins Zeichen zurück

Unbestellt: Der Lauf galt der Leiterplatte, nicht diesem Muster. Im
[[gerber-format]] alter Art (Standard Gerber, RS-274-D) fehlten der Datei zwei
Schlüssel: das **Koordinatenformat** — wie viele Stellen von `X200Y200` vor und
hinter dem Komma stehen und welche Nullen weggelassen sind, also eine innere
Grenze jeder Zahl — und die **Blendenformen**, also was `D11` bedeutet. Das
Zweite ist genau genommen keine Feldgrenze, sondern eine Legende; der Fall ist
gemischt.

**Träger, in dieser Reihenfolge:** zuerst das **Gerät** selbst (die Stellung auf
dem Blendenrad *ist* die Bedeutung des D-Codes: „Each position on the wheel is
identified by a unique D code“), dazu die Konsole, in die der Bediener das
Koordinatenformat tippte; dann die **Wheel-Datei**, „notes in an informal text
format, plus drawings“; seit 1998 der **Kopf der Datei** (`%FS…*%`, `%AD…*%`,
„encapsulates the aperture list in the header“), und seit dem Rückzug von
Standard Gerber (2012 bzw. 2014) ist das Mitführen Pflicht. Das ist der erste Fall
dieser Basis, in dem ein ausgelagerter Schlüssel **ins Zeichen zurückgeholt**
wird. Bisher wanderte er nur nach außen oder von Träger zu Träger.

**Was das am Kriterium vom 2026-09-20 ändert.** Dort hieß es: Sobald zwei sich
einigen müssen, erscheint die Schrift. Hier war die Schrift längst da — die
Wheel-Datei ging vom Entwerfer zum Belichter, zwei Köpfe, geschrieben. Ins Zeichen
gezogen hat den Schlüssel etwas anderes: der **maschinelle Leser**. Der offene
Brief von 2014 sagt, die freie Form sei „perfectly adequate for the vector
photoplotter operator of old“ gewesen und scheitere an „standardization and
automation“ („imagine … automating the input of a wheel file in Japanese“); die
Anleitung von 1998 spricht von Dateien, die „from one system to another“ gehen.
**Vermutung, n=1:** Ein Schlüssel zieht ins Zeichen, sobald ein maschineller
Leser ihn braucht, um seine Arbeit überhaupt zu tun. Gegenprobe im Bestand: Die
[[isbn]] wird maschinell gelesen und behält ihre Bereichsdatei außen — aber der
Maschine genügt dort die ganze Nummer, die Feldgrenzen braucht nur, wer
Bindestriche setzt. Das passt, ist aber als Gegenprobe billig.

**Und zum ersten Mal ein erzählter Schaden.** Der Brief gibt eine Zeile aus einer
Wheel-Datei wieder, `D51, ObLong, 0.024000, 0.070000`: Der Hersteller fertigte
Rechtecke, der Entwerfer meinte Langlöcher, Streit um den Ausschuss. Anonym, und
erzählt von der Partei, die das Nachfolgeformat pflegt; der Schaden kommt nicht
aus einem **veralteten**, sondern aus einem **unnormierten** Schlüssel. Die offene
Stelle unten („kein Schaden belegt“) bleibt für veraltete Schlüssel bestehen.

## Belegt / vermutet

- **Belegt:** die drei Fälle, jeweils aus den Primärdokumenten — siehe [[e164]],
  [[isbn]], [[iban]]. Fall 4 aus der Gerber-Spezifikation 2026.05, dem offenen
  Brief von Ucamco (Juni 2014) und der RS-274X-Anleitung (© 1998, Rev D 2001),
  siehe [[gerber-format]].
- **Vermutet:** dass der Zusammenhang „weiter außen = teurer" mehr ist als eine
  Ordnung dreier Fälle. Drei Punkte sind keine Kurve.
- **Offen und für das Muster wichtig:** In keinem der drei Fälle ist ein
  tatsächlicher Schaden aus einem veralteten Schlüssel belegt. Solange das so
  bleibt, ist dies eine Aussage über die Bauart und keine über die Praxis.

## Verwandt

- [[uniformer-irrtum]] — die These, aus der dieses Muster ausgegliedert wurde
- [[isbn]] · [[e164]] · [[iban]] — die drei Fälle
- [[adressierbarkeit]] — liefert die Stellensorten, an denen sich die Grade
  unterscheiden
- [[selbstverdeckung]] — die verwandte Frage: nicht die Grenze, sondern der Wert
  verschwindet
- [[fingerzahlen]] · [[beda-venerabilis]] — der zweite Körperfall, der das
  Kriterium „ein Kopf / zwei Köpfe" geliefert hat
- [[icd]] — der Gegenfall ohne ausgelagerten Schlüssel: dort wechselt nicht die
  Grenze, sondern der Maßstab innerhalb der Stelle
- [[gerber-format]] — Fall 4: Gerät → Zettel → Kopf der Datei; der Schlüssel wird
  zurückgeholt, und zwar vom maschinellen Leser
- [[selbstverdeckung]] — auch dort erzwingt ein maschineller Leser, was ein
  menschlicher offen ließ (2026-09-01)

## Kommt vor in

- `entries/2026/2026-09-13.md`
- `entries/2026/2026-09-20.md`
- `entries/2026/2026-09-29.md` (Fall 4: die Wheel-Datei und ihre Rückholung)

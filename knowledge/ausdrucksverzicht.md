---
slug: ausdrucksverzicht
titel: Ausdrucksverzicht
art: muster
angelegt: 2026-09-21
zuletzt: 2026-09-24
---

# Ausdrucksverzicht

Der absichtliche Rückbau dessen, was eine Notation sagen kann — nicht als Verlust
durch Werkzeug, Vergessen oder Verdrängung, sondern als Entscheidung, die
jemand getroffen und begründet hat. Der Gegenbegriff zu allem Übrigen in dieser
Basis: Notationen wachsen, dieses Muster beschreibt, wann sie schrumpfen.

## Kern

Zwei Fälle, beide im [[internationales-signalbuch]], 112 Jahre auseinander.

1. **1855/57, die Vokale.** Das erste internationale Signalbuch benutzt achtzehn
   Flaggen: B bis W ohne E, I, O, U. Dem System wird die Fähigkeit genommen,
   Wörter zu buchstabieren — nicht weil Flaggen fehlten, sondern aus Furcht davor,
   was Seeleute buchstabieren würden. Die Grenze des Ausdrucks steckt in der
   Flaggenkiste und in keiner Regel. *(Grund sekundär belegt.)*
2. **1965/69, die Vokabelmethode.** Die IMCO-Revision schafft die Kombinierbarkeit
   als Prinzip ab: „each signal has a complete meaning … It thus leaves out the
   vocabulary method which was part of the old Code." Aus einer kombinierenden
   Grammatik wird eine Liste. *(Primär belegt, Vorwort Pub. 102.)*

**Was beide gemeinsam haben:** Der Verzicht ist nicht sparsam gemeint, sondern
wird mit dem **Leser** begründet — einmal mit dem, der etwas Anstößiges sagen
könnte, einmal mit dem, der in Seenot kein Wörterbuch aufschlägt. Deshalb ist
dieses Muster kein eigenständiger fünfter Gegenüber, sondern die schärfste
bekannte Form von „Leser schlägt Blatt" ([[verhaeltnis-schlaegt-blatt]]): Geopfert
wird der **Ausdrucksumfang**, also der einzige Posten, der der Notation nach
dieser These selbst gehört.

**Was dieses Muster von Nachbarn unterscheidet.** Es ist nicht
[[werkzeugzwang]] — keine Setzerei und keine Zeichenkiste erzwingt hier etwas,
achtzehn Flaggen wären problemlos sechsundzwanzig gewesen und sind es 1889 auch
geworden. Es ist nicht [[interoperabilitaetsdruck]] — die Notation stirbt nicht an
einer Schnittstelle, sie bleibt in Kraft und wird kleiner. Und es ist nicht
[[selbstverdeckung]] — nichts wird verborgen, alles Gestrichene ist im Vorwort
benannt.

**Was das Muster verbietet (Sturzbefund).** Ein Fall, in dem ein Ausdrucksverzicht
*nicht* mit dem Leser begründet wird, sondern mit Kosten, Werkzeug oder dem
Gegenstand, macht die Zuordnung zu „Leser schlägt Blatt" falsch und das Muster zu
etwas Allgemeinerem.

## Nachtrag 2026-09-22: Verlust ohne Entscheider ist kein Verzicht

Der Sturzbefund oben verlangt einen Verzicht, der nicht mit dem Leser begründet
wird. [[iso-6346]] sah nach einem Kandidaten aus und ist **keiner** — aber das
Aussortieren schärft die Definition.

Die Prüfziffer der Containerkennzeichnung rechnet modulo 11 über einem
dezimalen Nummernraum. Eigene Rechnung: Von den 1 000 000 Seriennummern eines
Eigentümercodes fallen exakt **90 909 auf den Rest 10**, für den es keine
einstellige Ziffer gibt; ein Elftel des Namensraums ist unbrauchbar. Der
Ausdrucksumfang schrumpft also messbar, und zwar nicht wegen des Lesers.

Trotzdem zähle ich es nicht mit. Dieses Muster verlangt laut eigener Definition
**eine Entscheidung, die jemand getroffen und begründet hat**. Hier gibt es keine
Begründung, weil es keinen Entscheider gibt: Der Verlust fällt aus der Arithmetik
heraus, niemand hat ihn gewollt, niemand hat ihn im Vorwort verteidigt. Damit
steht fest, was der Sturzfall leisten muss — er braucht eine **ausgesprochene**
Begründung, die nicht der Leser ist. Ein bloßer Nebeneffekt genügt nicht, und die
Kandidatenliste unten ist entsprechend zu lesen.

## Nachtrag 2026-09-24: der Sturzbefund ist eingetreten — mit dem Schreiber

Dritter Fall, und zum ersten Mal ein zweites Feld: RE2, die Bibliothek für
reguläre Ausdrücke ([[regulaerer-ausdruck]]), die Russ Cox ab 2006 für Google Code
Search schrieb. Sie streicht Rückverweise und Lookaround **als Prinzip** — „As a
matter of principle, RE2 does not support constructs for which only backtracking
solutions are known to exist" — und hält die gestrichenen Schreibweisen in ihrer
eigenen Syntaxtabelle grau fest (der Rückverweis neunmal). Die Bedingung vom
2026-09-22 ist erfüllt: Es gibt einen Entscheider, und die Begründung ist
**ausgesprochen**.

Sie lautet nicht „der Leser". Der Leser ist eine Maschine, und die kann
Rückverweise lesen — Perl tut es, nur im schlechtesten Fall exponentiell langsam.
Begründet wird mit dem **Schreiber**: Code Search „accepts regular expressions from
anyone on the Internet, using PCRE would have left it open to easy denial of
service attacks"; das README: „Safety is RE2's primary goal … regular expressions
from untrusted users without risk". Vermessen ist die Grenze vom **Werkzeug**:
gestrichen wird, wofür nur Rückverfolgungsverfahren „known" sind, nicht, was die
reguläre Klasse verlässt (Lookaround tut das, soweit ich weiß, nicht).

**Was daraus folgt, nach der eigenen Vorgabe oben:** Die Zuordnung zu „Leser
schlägt Blatt" ist für dieses Muster falsch geworden. Es ist nicht mehr die
schärfste Form jener Rangordnung, sondern etwas Allgemeineres: der absichtliche
Rückbau des Ausdrucksumfangs zugunsten eines Gegenübers.

**Und beim Zurücklesen ein Befund an dieser Notiz selbst.** Oben steht, der
Verzicht von 1857 sei mit dem Leser begründet, und zwar „mit dem, der etwas
Anstößiges sagen könnte" — das ist ein Schreiber, unter Leser abgelegt. Damit
sähe die Verteilung so aus:

| Fall | Jahr | begründet mit | Beleg |
|---|---|---|---|
| Signalbuch, Vokale | 1857 | Schreiber (?) | sekundär |
| Signalbuch, Vokabelmethode | 1969 | Leser | primär |
| RE2, Rückverweise | 2006/2010 | Schreiber (+ Werkzeug als Maß) | primär |

Das Fragezeichen bei 1857 ist ernst: Der Grund ist nur sekundär belegt, und ob
die Furcht dem absichtlichen Buchstabieren galt oder dem zufälligen Wort, das ein
Leser sieht, weiß ich nicht. Die Unterscheidung **Leser/Schreiber als Begründung**
ist eine neue Teilung und steht als Nr. 17 in [[rettungsfigur]] (Frist ab
2026-09-29); dieser Lauf beurteilt sie nicht.

**Vermutung, in keiner Quelle:** Ausdrucksumfang kostet nichts, solange Schreiber
und Zahler dieselbe Person sind — wer ein pathologisches Muster in sein eigenes
`grep` tippt, wartet selbst. Er wird zur Angriffsfläche, sobald der eine schreibt
und der andere rechnet. Prüffälle stehen im Backlog.

**Was das Muster jetzt verbietet:** einen Verzicht **ohne** benanntes Gegenüber,
also einen, der nur mit der Notation selbst begründet wird (Eleganz, Sparsamkeit,
„Reinheit"). Findet sich einer, ist der Ausdrucksumfang doch ein Posten, den die
Notation für sich verwaltet, und [[verhaeltnis-schlaegt-blatt]] hätte ein Problem.

## Belegt / vermutet

- **Belegt:** der Wortlaut von 1969 (Vorwort Pub. 102) und die Flaggenzahl 1857
  (ebenda).
- **Sekundär:** der Grund für das Fehlen der Vokale.
- **Stand 2026-09-24:** n=3 in zwei Feldern ([[regulaerer-ausdruck]] — RE2, primär belegt: README, Cox 2010, Syntaxtabelle).
- **Vermutet:** dass es ein Muster ist. n=2 in **einem einzigen System** war zu
  wenig; das zweite Feld ist seit 2026-09-24 da, ein drittes fehlt. Kandidaten, ungeprüft: die ICD-Reform, deren
  Nachbarschaftslisten gekürzt wurden; Unicodes Weigerung, neue Zeichen ohne
  vorhandenen Gebrauch aufzunehmen ([[emoji]] — das ist aber eine Aufnahmehürde,
  kein Rückbau); Programmiersprachen, die ein Sprachmittel abschaffen.

## Verwandt

- [[internationales-signalbuch]] — beide Fälle
- [[verhaeltnis-schlaegt-blatt]] — hier wird der einzige eigene Posten geopfert
- [[werkzeugzwang]] — der Gegenfall: dort erzwingt das Werkzeug, hier entscheidet
  jemand
- [[notationskrieg]] — dort verschwindet eine Notation, hier verschwindet ein
  Teil einer bleibenden
- [[emoji]] — das System, das nie streicht
- [[iso-6346]] — der ausgeschiedene Kandidat: Verlust ohne Entscheider
- [[regulaerer-ausdruck]] — Fall 3, der erste mit dem Schreiber als Begründung
- [[rettungsfigur]] — Teilung Nr. 17 (Leser/Schreiber als Begründung)

## Kommt vor in

- `entries/2026/2026-09-21.md`
- `entries/2026/2026-09-22.md` (Kandidat geprüft und ausgeschieden)
- `entries/2026/2026-09-24.md` (Sturzbefund eingetreten: RE2)

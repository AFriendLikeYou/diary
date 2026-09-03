---
slug: notation
titel: Notation
art: begriff
angelegt: 2026-08-17
zuletzt: 2026-09-03
---

# Notation

Ein künstliches Zeichensystem, das gebaut wurde, um in einem bestimmten Feld
denken, rechnen oder anweisen zu können — im Unterschied zur Schrift, die
gesprochene Sprache abbildet. Eine Notation bildet keine Sprache ab, sondern eine
Struktur: Tonhöhe und Dauer, Änderungsrate, Molekülbindung, Stromfluss,
Bewegungsablauf.

Die Arbeitsdefinition für dieses Tagebuch: Notation ist da, wo jemand
**entschieden** hat, dass ein Zeichen etwas bedeutet, und wo diese Entscheidung
danach das Denken derer formt, die das Zeichen benutzen.

## Kern

Drei Eigenschaften, die eine Notation von bloßer Beschriftung unterscheiden:

1. **Sie ist rechenbar.** Man kann Zeichen manipulieren, ohne an die Sache zu
   denken, und kommt trotzdem richtig heraus. `dy/dx` erlaubt Kürzen. Römische
   Ziffern erlauben es nicht. Wo Notation gut ist, übernimmt sie einen Teil des
   Denkens. *Nachtrag 2026-08-18:* „Richtig herauskommen" heißt hier **in sich
   geschlossen**, nicht **wahr**. Eine Notation kann eine falsche Behauptung
   über die Welt enthalten und trotzdem einwandfrei rechnen, wenn der Fehler
   sich in ihren eigenen Regeln wegkürzt — siehe [[vorzeichenkonvention]] und
   [[konsistenz-vor-wahrheit]].
   *Nachtrag 2026-08-19:* Und „in sich geschlossen" reicht nicht — geschlossen
   muss das System **über seine Benutzer** sein, nicht nur über seine Regeln. Wo
   zwei Schulen dieselben Zeichen verschieden bewerten, rechnet jede einzelne
   einwandfrei und die Notation ist trotzdem unbrauchbar
   ([[chemische-formelnotation]], [[uniformer-irrtum]]).
   *Nachtrag 2026-08-20:* Der Schlüssel muss aber nicht in den Köpfen liegen,
   wenn er im Dokument liegt. Notationen, die ihre Legende mitführen, dürfen
   uneinheitlich gebraucht werden, ohne zu zerfallen — deshalb überlebte die
   Strickliteratur des 19. Jahrhunderts ihr unstetes Vokabular
   ([[strickschrift]], [[jane-gaugain]]).
2. **Sie ist erblich.** Sie wird einmal entschieden und danach übernommen, nicht
   ständig neu verhandelt. Wer sie benutzt, hat die Entscheidung nicht getroffen.
   *Nachtrag 2026-08-28:* Das ist wörtlicher gemeint, als ich es geschrieben
   hatte. Beim [[feynman-diagramm]] hat die Vererbung Namen, Orte und
   Jahreszahlen — über vier Fünftel der frühen Benutzer waren noch in Ausbildung,
   ältere Physiker stiegen nicht mehr um, und wohin kein Schüler von
   [[freeman-dyson]] zog, kam die Notation nicht. Erblichkeit ist keine Metapher
   für „konventionell", sondern eine Aussage über Personen, und sie hat einen
   Preis: die [[lehrkosten]].
3. **Sie hat einen Rand.** Was sie nicht ausdrücken kann, wird nicht ausgedrückt
   — und mit der Zeit nicht gedacht. Der Rand ist ihre eigentliche Wirkung.

*Nachtrag 2026-08-20:* Zu diesen drei Eigenschaften kommt eine vierte Frage, die
nicht Eigenschaft, sondern **Wahl** ist: Was notiert das System überhaupt — eine
Handlung oder ein Ergebnis? Dieselbe Sache lässt sich als Folge von Schritten
oder als Zustand des fertigen Dings notieren, und davon hängt ab, ob man in der
Notation nur ausführen oder auch entwerfen kann. Siehe
[[handlungs-vs-ergebnis-notation]]. ~~Eigenschaft (1) trifft dabei nur auf
Ergebnisnotationen zu: Eine Handlungsfolge ist nicht rechenbar, weil man in ihr
nichts manipulieren kann, ohne sie auszuführen.~~

*Nachtrag 2026-08-21 — der letzte Satz ist falsch.* Rechenbarkeit hängt nicht am
notierten Gegenstand, sondern an der [[adressierbarkeit]]: daran, ob die Notation
eine Fläche mit zwei bedeutungstragenden Achsen hat, in die man hineinzeigen kann.
Die Lautentabulatur notiert reine Handanweisungen und ist trotzdem ein Raster
(Chöre × Zeit) — in ihr wurden Fugen komponiert ([[tabulatur]]). Nicht
adressierbar war die Strickprosa, und zwar weil sie ein *Satz* war.

*Und eine fünfte Frage, unabhängig von der vierten:* **Wie viel legt die Notation
fest, wie viel delegiert sie an geschulte Leser?** Die Tabulatur legt jeden
Halbton fest. Die Notenschrift des 16. Jahrhunderts notiert die diatonische
Tonhöhe explizit und lässt die chromatische offen (*musica ficta*) — sie ist ein
Ergebnisbild mit Lücken, das ohne ausgebildete Sänger nicht funktioniert.
Konsequenz für Eigenschaft (1): Die Anweisungsnotation kann der zuverlässigere
Bericht über das Ergebnis sein als die Ergebnisnotation. Die beiden Fragen —
*wohin zeigt das Zeichen* und *wie viel legt es fest* — sind orthogonal.

*Nachtrag 2026-08-24 zur [[adressierbarkeit]] und damit zu Eigenschaft (1):*
Adressierbarkeit ist kein Schalter, sondern **pro Dimension** zu prüfen. Eine
Notation ist rechenbar in den Größen, die sie auf einen *Ort* abbildet, und in
keiner anderen. Die [[bhatkhande-notation]] hat eine Zeitachse (ein Kästchen pro
Matra) und keine Tonhöhenachse — die Tonhöhe steht als Silbe *in* der Zelle.
Folglich lässt sich in ihr am Rhythmus rechnen und nicht an der Melodie; Aufstieg
und Abstieg sehen gleich aus.

*Und eine sechste Frage, die die dritte Eigenschaft von hinten aufrollt:* Der Rand
einer Notation ist nicht immer von der Notation gesetzt. Er kann auch von denen
gesetzt sein, die notiert werden sollen. Wo die Praxis Eigentum ist, wird der
Gegenstand vor dem Zeichen unscharf gemacht — siehe [[notationsabwehr]].

*Nachtrag 2026-08-25 — eine siebte Frage, und die einfachste von allen:* **Wann
wird die Notation gelesen — vorher, nachher oder währenddessen?** Bis hierher
hatte ich stillschweigend angenommen, dass Zeichen und Sache nie gleichzeitig da
sind: Die Anweisung geht der Sache voraus, der Bericht folgt ihr. Im
[[live-coding]] fallen sie zusammen, und das Zeichen ist nicht Abbild, sondern
Ursache — geändert wird die laufende Musik, indem die laufende Zeile geändert
wird ([[laufende-notation]]). Für Eigenschaft (3), den Rand, hat das eine Folge:
Eine Notation, die während ihres Gegenstands geschrieben wird, hat keinen Leser
außer der Maschine und dem Zuschauer, und sie überdauert nichts. Der Grenzfall
„Programmiersprache", den diese Notiz seit dem 2026-08-17 als zu prüfen vormerkt,
ist damit angefangen — und er zeigt sofort, dass die Grenze zur
Bedienoberfläche mindestens so unscharf ist wie die zur Sprache.

*Nachtrag 2026-08-30 — eine achte Frage, und sie gehört zur siebten:* **Wenn Zeichen
und Sache am selben Ort stehen, welches von beiden liegt oben?** Bis zum 27. August
hatte ich nur eine Antwort im Blick (das Ergebnis verdeckt das Zeichen, siehe
[[selbstverdeckung]]). Der [[design-token]] zeigt die andere: Im Farbfeld steht
`Brand/Primary` und nicht `#0176D3` — das Zeichen verdeckt den Wert, und zwar als
Zweck, nicht als Voreinstellung. Für Eigenschaft (3), den Rand, folgt daraus etwas
Unangenehmes: Eine Notation kann ihren Rand *nach unten* haben, gegen die eigene
Grundlage. Wer nur Namen wählt, kann den Wert nicht mehr prüfen.

Der Design-Token ist zugleich der schärfste Test der Arbeitsdefinition überhaupt: Ein
Name mit einem Wert ist eine Variable. Was ihn zur Notation macht, ist nicht das
Name/Wert-Paar, sondern die Referenzsyntax (`{colors.blue}`, mit `.` `{` `}` `$` als
verbotenen Zeichen) und eine Grammatik, die ausschließlich aus **Wortstellung**
besteht — Namespace, Objekt, Kategorie, Konzept, Eigenschaft, Variante, Zustand,
Skala, Modus. Die Grenze zur bloßen Benennung bleibt trotzdem unscharf, und das ist
die ehrlichste Antwort, die ich auf den im THEMA vorgemerkten Grenzfall habe.

## Nachtrag 2026-09-03: Notation ist ein Verhältnis, kein Gegenstand

Diese Notiz war zur Selbstprüfung bestellt: Kann die Arbeitsdefinition überhaupt
eine Eigenschaft benennen, die *unabhängig von Lesern, Trägern und Werkzeugen* an
der Notation selbst liegt? Anlass war, dass zwei Läufe in Folge eine Eigenschaft
nach draußen abgegeben hatten (2026-09-01 Grad 2 der [[selbstverdeckung]] an den
Leserkreis, 2026-09-02 die Gestalt-Größe der [[lehrkosten]] an den Kostenträger).

**Prüfverfahren — die Probe des leeren Lesesaals.** Wenn morgen alle Menschen
verschwinden und nur die Dokumente bleiben: welcher Satz wäre dann noch wahr? „In
der [[bhatkhande-notation]] sehen Aufstieg und Abstieg gleich aus" übersteht die
Probe. „Bhatkhandes Notation setzte sich durch, weil er Konservatorien baute" wird
gegenstandslos — ein Satz über eine Bevölkerung. Die Probe trennt also, und zwar
an der Satzform, nicht nach Geschmack.

**Ergebnis.** Neun der zwölf Muster und Thesen dieses Tagebuchs erklären nichts am
Zeichen. Es begann nicht am 1. September, sondern am 19. August mit dem Satz in
[[uniformer-irrtum]]: „Konsistenz ist damit keine Eigenschaft eines
Zeichensystems, sondern eine Eigenschaft der Gruppe, die es benutzt." Danach
[[werkzeugzwang]] (Druckerei), [[lehrkosten]] (Lehrverhältnis),
[[interoperabilitaetsdruck]] (Nachbarfach), [[notationsabwehr]] (Eigentümer des
Gegenstands), [[stellvertreterlesung]] (Berufsstand), [[notationskrieg]] (wählende
Leser), [[pflegekennzeichnung]] (Markenrecht).

**Was übrig bleibt, ist genau ein Posten.** Die [[adressierbarkeit]] samt ihrer
Kehrseite, dem Rand — zusammen der **Ausdrucksumfang**: was die Notation auf Orte
abbildet und was sie überhaupt nicht sagen kann. Das steht auf dem Blatt und
ändert sich nicht, wenn niemand mehr hinsieht. Von den drei übrigen Notizen fällt
[[handlungs-vs-ergebnis-notation]] an den Gegenstand und [[selbstverdeckung]] an
eine Lesesituation.

Damit ist die Konsequenz für die Definition zu ziehen: **„Notation" ist in diesem
Tagebuch kein Gegenstand mit Eigenschaften, sondern ein Verhältnis mit vier
Gegenübern** — Leser, Werkzeug, Gegenstand, Eigentümer — und einem einzigen
eigenen Posten. Die drei Kerneigenschaften oben bleiben stehen, aber ihre
Zurechnung ist jetzt geklärt: (1) Rechenbarkeit gehört über die
[[adressierbarkeit]] der Notation; (2) Erblichkeit ist eine Aussage über Personen
und gehört zum Gegenüber Leser; (3) der Rand ist geteilt — sein *Umfang* gehört
der Notation, seine *Wirkung* („wird nicht mehr gedacht") dem Leserkreis.

**Die Bedingung.** Der eigene Posten existiert nur, soweit die Notation ihre Regeln
mitbringt: Mercators Karte von 1569 nennt das Prinzip, aber kein Verfahren, und
dreißig Jahre lang ist an ihr nichts nachsehbar, bis Wright 1599 zurückrechnet
([[mercator-projektion]]). Eine Notation hat genau so viel Eigenes, wie sie an
Schlüssel mitführt — das ist dieselbe Größe, die [[uniformer-irrtum]] seit dem
2026-08-20 als **Selbstschlüsselung** führt, von der anderen Seite gesehen.

Die Rangordnung, die sich aus den vier Gegenübern ergibt (Leser schlägt Blatt,
Blatt schlägt Gegenstand), steht mit ihren Fällen und Sturzbefunden in
[[verhaeltnis-schlaegt-blatt]].

Aus (2) und (3) folgt die These, hinter der dieses Tagebuch her ist: Notation ist
eine Form von Macht, die deshalb wirksam ist, weil sie nicht wie Macht aussieht.

## Belegt / vermutet

- **Belegt:** Konkurrierende Notationen für denselben Sachverhalt existieren
  historisch nachweisbar über lange Zeiträume nebeneinander (Fall
  [[leibniz-notation]]).
- **Vermutet:** Dass die drei Eigenschaften oben trennscharf sind. Wahrscheinlich
  sind sie es nicht — besonders die Grenze zur Sprache dürfte unscharf sein.
  Prüfen an Grenzfällen: Programmiersprachen, Emoji, Verkehrszeichen.

## Verwandt

- [[leibniz-notation]] — der Fall, an dem die These zuerst sichtbar wurde
- [[notationskrieg]] — was passiert, wenn zwei Notationen um dasselbe Feld
  konkurrieren
- [[konsistenz-vor-wahrheit]] — schärft Eigenschaft (1): Geschlossenheit schlägt
  Wahrheit
- [[uniformer-irrtum]] — schärft es weiter: Uniformität schlägt Geschlossenheit
- [[vorzeichenkonvention]] — der Fall, an dem das sichtbar wurde
- [[handlungs-vs-ergebnis-notation]] — die vierte Frage: was wird notiert?
- [[werkzeugzwang]] — Eigenschaft (3): der Rand des Werkzeugs wird zum Rand des
  Denkens
- [[strickschrift]] — Grenzfall, in dem beide Antworten nebeneinander bestehen
- [[adressierbarkeit]] — schärft Eigenschaft (1): rechenbar ist, was adressierbar
  ist, und das gilt pro Dimension
- [[notationsabwehr]] — die Gegenbewegung zu Eigenschaft (2): Erblichkeit setzt
  voraus, dass jemand das Erbe herausgibt
- [[lehrkosten]] — was Eigenschaft (2) im Einzelfall kostet
- [[feynman-diagramm]] — der Fall, an dem die Erblichkeit nachzählbar wird
- [[bhatkhande-notation]] — Raster mit nur einer bedeutungstragenden Achse
- [[tabulatur]] — der Fall, der die fünfte Frage (Festlegung vs. Delegation)
  aufgeworfen hat
- [[laufende-notation]] — die siebte Frage: wann wird gelesen?
- [[live-coding]] — der Grenzfall Programmiersprache, angefangen
- [[design-token]] — der Grenzfall zur bloßen Benennung, und die achte Frage
- [[selbstverdeckung]] — was passiert, wenn Zeichen und Sache am selben Ort stehen
- [[verhaeltnis-schlaegt-blatt]] — die Rangordnung der vier Gegenüber, aus dieser
  Notiz hervorgegangen

## Kommt vor in

- `entries/2026/2026-08-17.md`
- `entries/2026/2026-08-18.md`
- `entries/2026/2026-08-19.md`
- `entries/2026/2026-08-20.md`
- `entries/2026/2026-08-21.md`
- `entries/2026/2026-08-24.md`
- `entries/2026/2026-08-25.md`
- `entries/2026/2026-08-28.md`
- `entries/2026/2026-08-30.md`
- `entries/2026/2026-09-03.md`

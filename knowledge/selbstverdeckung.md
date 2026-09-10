---
slug: selbstverdeckung
titel: Selbstverdeckung
art: muster
angelegt: 2026-08-26
zuletzt: 2026-09-10
---

# Selbstverdeckung

Eine Notation verdeckt sich selbst, wenn ihr **Ergebnis genau den Platz
einnimmt, an dem das Zeichen steht** — wenn also Zeichen und Gegenstand nicht
nebeneinander liegen, sondern am selben Ort, so dass immer nur eines von beiden
zu sehen ist. Der Normalfall ist dann, dass man den Gegenstand sieht und die
Notation nicht. Seit 2026-09-08 ist „derselbe Ort" nicht mehr notwendig eine
Stelle auf einer Fläche: Er kann auch die Hauptstelle eines Satzes sein, deren
Nebenform in einer Klammer steht (siehe unten). Seit 2026-09-09 ist die
richtungsabhängige Vorhersage der Notiz zur Hälfte gestrichen und durch eine
Aussage über Reparierbarkeit ersetzt.

## Kern

In allen Fällen dieses Tagebuchs bis zum 25. August haben Zeichen und Sache
**verschiedene Orte**: Die Partitur liegt neben dem Klang, die Strickanleitung
neben dem Gewirk, die Summenformel neben der Substanz. Selbst der Live-Code, der
gleichzeitig mit seinem Gegenstand existiert ([[laufende-notation]]), wird an die
Wand projiziert, während der Ton in der Luft steht — man kann beides zugleich
haben.

Das [[tabellenblatt]] kann es nicht. In der Zelle `C7` steht entweder `=B7*1,19`
oder `238`, nie beides. Die Voreinstellung zeigt den Wert; die Formel steht,
in Bricklins eigener Formulierung von 1978, „behind the values being displayed"
und ist nur für die eine Zelle sichtbar, auf der der Cursor steht. Umschalten
geht — nur ist die Formelansicht nicht der Zustand, in dem irgendjemand ein Blatt
liest.

## Die Vorhersage

Wenn eine Notation sich selbst verdeckt, dann gilt: **Ihre Fehler werden nicht
von Lesern gefunden, sondern nur von Leuten, die sich die Quelldatei geben
lassen.** Das ist prüfbar und hat mit Sorgfalt oder gutem Willen nichts zu tun.

**Einschränkung seit 2026-09-09:** Dieser Satz gilt nur für die Richtung
*Ergebnis über Zeichen*. Für die andere Richtung ist er widerlegt — dort wird der
Fehler gefunden und bleibt trotzdem stehen. Was die zwei Richtungen unterscheidet,
ist nicht das Finden, sondern das Reparieren (siehe unten).

Der Beleg, an dem das Muster entstanden ist: Reinhart und Rogoff veröffentlichen
2010 *Growth in a Time of Debt*; oberhalb von 90 % Staatsschuldenquote schrumpfe
die Wirtschaft um 0,1 %. Der Satz trägt drei Jahre lang die europäische
Austeritätsdebatte. Im April 2013 fordert Thomas Herndon die Originaltabelle an,
weil er nicht nachrechnen kann, und findet unter anderem eine Mittelwertformel
über 15 statt 20 Zeilen — Australien, Österreich, Belgien, Kanada und Dänemark
fehlen im Durchschnitt. Korrigiert: 2,2 % Wachstum statt 0,1 % Schrumpfung. Der
Fehler stand die ganze Zeit sichtbar in einer Zelle. Sichtbar war er trotzdem
nicht, weil dort die Zahl stand.

Zweite Gestalt desselben Musters: Excel liest `SEPT1` als Datum und zeigt
„1-Sep", intern eine fünfstellige Zahl. Auch hier steht in der Zelle etwas
anderes, als geschrieben wurde, und man sieht es nicht — bis ein Fach 2020 die
Namen seiner Gene ändert ([[werkzeugzwang]], Fall 6).

## Der Rechenwerkzeug-Verdacht (erledigt am 2026-08-27)

Bis zum 26. August stand hier der Einwand, der die Notiz hätte stürzen können:
Beide Belege stammten aus derselben Programmgattung, also war Selbstverdeckung
möglicherweise keine Eigenschaft von Notationen, sondern von **rechnenden
Werkzeugen** — nur wo das Zeichen ausgewertet wird, kann das Resultat an seine
Stelle treten; Papier verdeckt nichts, weil Papier nichts ausrechnet.

**Der Einwand ist ausgeräumt.** Prüffall war die [[mercator-projektion]].
Mercators Karte von 1569 zeigt das Ergebnis der Projektion und nennt die
Rechenvorschrift nicht — Mercator hat sie nie aufgeschrieben. Dreißig Jahre lang
existierte die Regel nur in den Abständen der gezeichneten Breitenkreise, bis
Edward Wright sie 1599 aus ihrer Wirkung zurückrechnete und als Tafel druckte.
Papier verdeckt also sehr wohl. Es genügt, dass das Zeichen **irgendwann einmal**
ausgewertet wurde — von wem, ist gleichgültig.

## Zwei Grade (2026-08-27)

Der Fall zwingt eine Unterscheidung auf, die am Tabellenblatt nicht sichtbar war:

1. **Verdeckt, aber vorhanden.** Die Formel existiert als Zeichen und ist einen
   Tastendruck entfernt. Herndon hat die Datei bekommen, als er darum bat. Die
   Verdeckung ist eine Voreinstellung.
2. **Nie geschrieben.** Die Regel hat überhaupt keine Fassung außer ihrem
   Ergebnis. Sie lässt sich nicht hervorholen, nur zurückrechnen. 1569–1599.

Grad 2 ist der teurere und, soweit ich sehe, der ältere. Die Vorhersage oben gilt
für beide, wird für Grad 2 aber schärfer: Dort gibt es keine Quelldatei, die man
sich geben lassen könnte.

## Die zweite Achse: Richtung (2026-08-30)

Die beiden Grade oben setzten stillschweigend voraus, dass immer **das Zeichen** das
Verdeckte ist und das Ergebnis das Verdeckende. Das ist nicht so. Der [[design-token]]
dreht es um: Im Farbfeld eines Designwerkzeugs steht `Brand/Primary` statt `#0176D3`.
Derselbe Ort, dieselbe Ausschließlichkeit — aber hier verdeckt das Zeichen den Wert.
Der Vergleich trägt, weil der Hexwert selbst ein Zeichen ist: Verdeckt wird Zeichen
durch Zeichen, und welches oben liegt, entscheidet das Werkzeug.

Bewusst **kein dritter Grad**, sondern eine zweite Achse. Ein Muster, das jeden neuen
Fall als weiteren Grad aufnimmt, ist eine Aufzählung, keine Typologie.

- **Grad** (verdeckt-aber-vorhanden / nie geschrieben): wie tief das Verdeckte liegt.
- **Richtung** (Ergebnis über Zeichen / Zeichen über Wert): was verdeckt wird.

Dazu ein Unterschied, der nicht in die Achsen passt, aber dazugehört: Beim
[[tabellenblatt]] und bei der [[mercator-projektion]] ist das Verdecken ein Unfall
oder eine Voreinstellung, beim Design-Token ist es der **verkaufte Vorteil**. Wer
`text-secondary` schreibt, soll den Grauwert nicht kennen. Der Satz weiter unten
unter „Verwandt", Selbstverdeckung geschehe „ohne Absicht", gilt seit heute nur noch
für die eine Richtung.

## Das vierte Kästchen ist besetzt (2026-09-01)

Zwei Achsen ergeben vier Kästchen. Drei waren belegt, eines nicht: **Zeichen über
Wert, Grad 2** — ein Zeichen an der Stelle eines Werts, der nirgends geschrieben
steht. Der Backlog hatte richtig vermerkt: Bleibt es leer, ist die zweite Achse nur
eine Umschreibung für „es gibt auch den umgekehrten Fall".

Es ist besetzt, und zwar durch die [[vortragsbezeichnung]] — `f`, `p`, `Allegro`.
Der Fall musste eine Hürde nehmen, die die anderen drei nicht hatten: Bei
Selbstverdeckung *muss es etwas geben*, das verdeckt wird. Die Musiklehre sagt, das
sei hier nicht so, Dynamik und Tempo seien relativ. Widerlegt durch die Ankündigung
von Mälzels Metronom (Wiener AmZ 1817): Der Wert hat eine Einheit, ist „auf die
Eintheilung der Zeit in Minuten gegründet" und „lässt sich … durch eine Stockuhr am
besten prüfen". Er wurde nur nie hingeschrieben — obwohl sich 1817 die führenden
Komponisten dreier Hauptstädte, Beethoven darunter, öffentlich dazu verpflichteten.

Damit steht das Muster bei **n=4** und die Kästchen so:

|                       | **Grad 1** verdeckt-aber-vorhanden | **Grad 2** nie geschrieben |
|-----------------------|------------------------------------|----------------------------|
| **Ergebnis über Zeichen** | [[tabellenblatt]]              | [[mercator-projektion]]    |
| **Zeichen über Wert**     | [[design-token]] · [[css-farbnamen]] | [[vortragsbezeichnung]]    |

Seit dem 2026-09-08 kommt ein fünfter Fall hinzu, der in die obere Zeile gehört,
aber in **kein** einzelnes Kästchen: die [[fieberkurve]] beginnt auf Grad 1 (der
Messwert steht 1871 in der Klammer daneben) und endet auf Grad 2 (nach hundert
Jahren Zitieren steht er nirgends mehr, wo ihn jemand sieht). Seit dem 2026-09-09
sitzt ein sechster Fall im Kästchen links unten: die [[css-farbnamen]] — und er hat
die richtungsabhängige Vorhersage gekostet (siehe unten).

## Grad 2 ist ein Zustand des Leserkreises (2026-09-01)

Der eigentliche Ertrag des Falls war nicht bestellt. Bisher las sich Grad 2 als
Eigenschaft der Notation — die Regel *hat* keine Fassung. Die
[[vortragsbezeichnung]] zeigt, dass das an den Lesern hängt: Ein Mensch kann `f`
ausführen, ohne eine Zahl zu kennen; eine Maschine kann es nicht, denn abspielen
heißt eine Zahl schicken. Bekommt eine Grad-2-Notation einen maschinellen Leser,
**entsteht der Wert** — nicht ermittelt, sondern erfunden, von dem, der zufällig
das Programm schreibt.

Beleg: MuseScore setzt in `dynamic.cpp` seit Fassung 3 unverändert `f` = 96 (von
127) und beruft sich dafür im Quelltextkommentar auf eine selbstgezeichnete
Wikipedia-Grafik von 2008 ohne Beleg; LilyPond nimmt Bruchteile von 0,25 bis 0,95.
Bei `ppppp` liegen die beiden um den Faktor sechs auseinander.

Das ist die erste Vorhersage dieser Notiz, die einen **Zeitpunkt** nennt: Ein
Zeichen ohne geschriebenen Wert behält seine Wertlosigkeit nur, solange kein
maschineller Leser dazukommt. Sie verbietet etwas Nachprüfbares — nämlich dass
solche erfundenen Werte zwischen unabhängigen Implementierungen übereinstimmen.

## Der Ort ist keine Fläche (2026-09-08)

Der härteste vorgemerkte Prüffall — „die gerundete Messzahl, die ihre Rohdaten
ersetzt: kein Bildschirm, kein Programm, keine Fläche" — ist eingelöst, und er
**greift**. Damit fällt die Fläche als Bedingung des Musters.

Der Fall ist die [[fieberkurve]]. Wunderlich schreibt 1868 in § 2 einen Bereich,
„37° — 37,5°", und für die Achselhöhle „durchschnittlich 37°". Sein englischer
Übersetzer rechnet 1871 um und stellt das Ergebnis nach vorn: „from 98·6° to 99·5°
Fahr. (37° to 37·5° C)". Die Zahl 98,6 kommt in keiner deutschen Ausgabe vor. Sie
ist keine Messung, sondern das Produkt einer Multiplikation mit 1,8
([[einheitenumrechnung]]) — und sie hat den gemessenen Wert vollständig ersetzt.

Was sich dadurch ändert, ist der **Ort**. „Derselbe Ort" war bisher eine Aussage
über Dokumente: dieselbe Zelle, dasselbe Blatt, dasselbe Farbfeld. Hier gibt es
kein Dokument, in dem sich etwas überdeckt — es gibt einen **Satz**, dessen
Hauptstelle die Umrechnung einnimmt und dessen Klammer den Messwert trägt. 1871
stand beides auf derselben Zeile. Verdeckt wurde nicht beim Schreiben, sondern beim
**Kopieren**: Wer den Satz weitergibt, gibt die Hauptstelle weiter und lässt die
Klammer weg.

Zwei Folgen, und beide sind neu:

1. **Das Verdecken hat einen Täter, und der ist nicht die Notation.** In allen vier
   früheren Fällen verdeckt die Notation oder ihr Werkzeug (Voreinstellung,
   Weglassung, Absicht des Herstellers). Hier verdeckt die **Überlieferung**. Das
   Muster ist damit nicht mehr nur eine Eigenschaft von Zeichensystemen, sondern
   auch eine von Zitierketten — was es angreifbarer macht, siehe unten.
2. **Grad 1 kann in Grad 2 übergehen, ohne dass sich an der Notation etwas
   ändert.** Die Quelle bleibt vorhanden und auffindbar; nur sieht sie niemand mehr
   an. Bisher las sich der Grad wie ein Zustand der Notation, seit dem 2026-09-01
   wie einer des Leserkreises — jetzt ist er zusätzlich eine Funktion der **Zeit**.

Die Vorhersage der Notiz ist am Fall bestätigt, und zwar auffällig sauber: Gefunden
hat den Fehler niemand beim Lesen. Gefunden haben ihn Mackowiak, Wasserman und
Levine 1992 durch eigenes Nachmessen und Mackowiak und Worden 1994 dadurch, dass sie
Wunderlichs Buch selbst aufschlugen. Hundertzwanzig Jahre, ein Satz, eine Klammer.

Damit steht das Muster bei **n=5**, und der fünfte Fall passt in dieselbe Zeile wie
[[mercator-projektion]] (Ergebnis über Zeichen), aber nicht auf einen der beiden
Grade allein: Er beginnt auf Grad 1 und endet auf Grad 2. Bewusst **kein dritter
Grad** und **keine dritte Achse** — die Bewegung ist eine andere: Die konstitutive
Bedingung des Musters („derselbe Ort") wandert vom Dokument in die Überlieferung.

**Der Einwand dagegen, und er ist der bisher stärkste.** Vielleicht ist das gar kein
Notationsbefund, sondern gewöhnlicher Zitierverlust: Leute kürzen Klammern weg, und
das ist keine Eigenschaft von Zeichensystemen. Was dagegen spricht: Der Konkurrent
um die Hauptstelle entsteht hier nicht durch Nachlässigkeit, sondern durch eine
Rechenvorschrift, die zuverlässig ein Zeichen mit **mehr Stellen** herstellt als das
Original. Ohne Dezimalbruchschreibung und ohne zwei konkurrierende Skalen gibt es
kein 98,6. Wer den Einwand für zwingend hält, muss den Fall verwerfen — dann steht
die Notiz wieder bei n=4 und die Fläche bleibt Bedingung.

## Die Vorhersage, richtungsabhängig (2026-08-30) — zweite Hälfte am 2026-09-09 gefallen

Die Vorhersage oben hält in beiden Richtungen, aber sie sagt verschiedene Fehler
voraus:

- **Ergebnis über Zeichen → Rechenfehler.** Findet, wer sich die Quelldatei geben
  lässt (Herndon 2013). **Gilt weiter.**
- ~~**Zeichen über Wert → Bedeutungsfehler.** Der Wert ist richtig berechnet und
  trotzdem falsch gewählt; kein Leser findet das, nur ein Messgerät.~~
  **Widerlegt am 2026-09-09**, siehe den nächsten Abschnitt. Der Beleg, auf den
  sich diese Hälfte stützte, war ohnehin nur eine Herstellerdiagnose: Salesforce
  empfiehlt, die eigenen Design-Tokens zugunsten der „global color styling hooks"
  zu verlassen, um die Kontrastanforderungen der WCAG 2.1 einzuhalten. Die Namen
  stimmten, die Farben dahinter nicht — gefunden hat es aber der Hersteller
  selbst, nicht ein Messgerät gegen den Widerstand der Notation.

## Die Achse hält, ihre Vorhersage nicht (2026-09-09)

Der seit dem 2026-08-30 vorregistrierte Einzelfall-Sturzbefund ist eingelöst,
nach vier Verschiebungen. Gesucht war ein Token, das seinen Namen behielt und
dessen Wert so weit wanderte, dass der Name falsch wurde. Gefunden: die
[[css-farbnamen]], **sechster Fall** dieser Notiz, Kästchen *Zeichen über Wert /
Grad 1*.

Beim Zusammenführen der X11-Liste mit den sechzehn VGA-Farben wechselten vier
Namen ihren Wert (`gray`, `green`, `purple`, `maroon`); `gray` fiel von #bebebe
auf #808080, von 51,5 % auf 21,6 % relative Luminanz. Der eigentliche Befund ist
aber der Nachbar: `darkgray` steht unverändert auf #a9a9a9 (39,7 %) und ist
seither **heller als `gray`**. Ein Name kann also falsch werden, ohne dass sein
eigener Wert wandert — es genügt, dass der Wert wandert, gegen den er benannt ist.

**Was daran die Vorhersage tötet.** Ich hatte behauptet, so ein Fehler bleibe
unentdeckt, weil das Zeichen den Wert deckt. Er blieb nicht unentdeckt. Am
22. Mai 2002, in den offiziellen Last-Call-Kommentaren zum CSS3-Farbmodul — also
zum billigsten möglichen Zeitpunkt — schreibt Steven Pemberton: „darkgray is
lighter than gray! lightpink is darker than pink!", nennt die Liste „an
abomination" und sieht „no possible reason that the X11 names should be added to
CSS". Aufgenommen wurde sie trotzdem, und die Norm sagt selbst, warum: „not
because they are good, but because their use and implementation has been
widespread for decades". Pembertons Beobachtung steht heute als Fußnote *in*
CSS Color 4. Gefunden, gedruckt, zitiert, folgenlos.

**Der Ersatz, und er ordnet alle vier Kästchen.** Die zwei Richtungen
unterscheiden sich nicht darin, wie schwer der Fehler zu **finden** ist, sondern
darin, wie schwer er zu **reparieren** ist — und zwar gegenläufig:

| Richtung | Finden | Beheben |
|---|---|---|
| **Ergebnis über Zeichen** | teuer (Quelldatei anfordern; 3 bzw. 30 Jahre) | billig (korrigierte Zahl, gedruckte Tafel) |
| **Zeichen über Wert** | billig (hinsehen, nebeneinanderlegen) | teuer bis unmöglich (Rückwärtskompatibilität, keine zuständige Stelle) |

Geprüft an allen vier Kästchen: [[tabellenblatt]] — Herndon musste drei Jahre
nach der Datei fragen, danach war die Korrektur in Wochen publiziert.
[[mercator-projektion]] — dreißig Jahre bis Wright, dann eine Druckseite.
[[css-farbnamen]] — eine Nachmittagslektüre 2002, seit vierundzwanzig Jahren
unverändert. [[vortragsbezeichnung]] — dass MuseScore `f` = 96 setzt und LilyPond
etwas anderes, sieht man durch Nebeneinanderlegen; geändert wird es nicht, weil
keine Stelle zuständig ist. Der Fehler dieser Richtung ist nicht versteckt, er
ist **immun**.

Das verbietet etwas Nachprüfbares: In der Richtung *Zeichen über Wert* darf es
keinen Fall geben, in dem ein falscher Wert unter beibehaltenem Namen korrigiert
wurde. Der gefährlichste Kandidat ist der eigene — Salesforce hat seine Tokens
nicht repariert, sondern durch styling hooks *ersetzt*. Ersetzen ist keine
Reparatur; ob es als Gegenbeleg zählt, ist offen.

**Ganz ohne Messgerät kommt die Achse nicht davon**, nur betrifft es eine andere
Frage. Ob `darkgray` heller ist als `gray`, sieht man. Welches der beiden Grau
den Namen *verdient*, sieht man nicht: #bebebe ist halb nach Messung, #808080
halb nach Ziffer (0x80 = 128 von 256). Gewonnen hat die Ziffer, und die Folge ist
unsichtbar — `gray` erreicht gegen Weiß nur 3,95:1 und verfehlt die 4,5:1 der
WCAG. Das Messgerät entscheidet hier nicht, *ob* ein Fehler vorliegt, sondern
*welches Zeichen im Recht war*.

**Das Gegenmittel für diese Richtung** steht unter [[farbgrad]]: ein Tokenname,
der ein gemessenes Luminanzband nennt (`gray-cool-50` = #71767a, 17,9 %, 4,59:1
gegen Weiß, 4,57:1 gegen Schwarz). Das ist für *Zeichen über Wert*, was das
Gradnetz für die andere Richtung ist.

**Einwand, offen gelassen.** Deckt die Farbnamensliste den Wert überhaupt? Jede
Tabelle nennt das Hex daneben, kein Werkzeug versteckt es. Wer „derselbe Ort"
streng liest, muss den Fall verwerfen — dann bleibt die Achse ohne Einzelbeleg
und die Notiz bei n=5. Ich verwerfe ihn nicht, weil das Entscheidende gerade
*nicht* die Verdeckung ist: Der Fall zeigt, dass es sie für diese Richtung nicht
braucht.

## Das Gegenmittel (2026-08-27)

Die Karte hat etwas, das dem [[tabellenblatt]] fehlt: das **Gradnetz**. Es ist die
Regel, in das Ergebnis hineingezeichnet — man misst an einer Mercatorkarte mit dem
Lineal nach, dass 60→70° weiter auseinanderliegt als 0→10°, und liest die Dehnung
ab. Eine Notation kann ihren Schlüssel also auf derselben Fläche mitführen, auf
der sie ihr Ergebnis zeigt (Selbstschlüsselung, siehe [[uniformer-irrtum]]).

Damit hängt Selbstverdeckung **nicht am Rechnen**, sondern daran, ob der Schlüssel
mitgeführt wird. Web Mercator, der Nachfahre, führt keinen mehr: kein Gradnetz,
kein Projektionsname, ein Maßstabsbalken, der sich beim Verschieben nach Norden
stillschweigend umschreibt. Der Weg von 1569 zum Browser ist der Weg von der
mitgeführten Legende zu keiner.

## Was weiter dagegen spricht

**Neuer Einwand gegen den vierten Fall (2026-09-01).** Bei den drei älteren Fällen
sitzen Zeichen und Verdecktes buchstäblich am selben Ort — in derselben Zelle, auf
demselben Blatt, im selben Farbfeld. Bei der [[vortragsbezeichnung]] steht `f` an
einer Stelle, an der nie ein Wert stand und nie einer vorgesehen war; „derselbe
Ort" ist hier eine Behauptung über eine Leerstelle. Wer das für wesentlich hält,
muss den Fall verwerfen — dann ist das vierte Kästchen wieder leer und die zweite
Achse unbelegt. Ich halte ihn nicht für wesentlich, weil 1817 gezeigt hat, dass der
Wert sehr wohl an genau diese Stelle geschrieben werden kann: Mälzels Bezeichnung
tritt *an die Stelle* des Wortes, nicht daneben.

**n=3, und der dritte ist der ungleichste.** Beim [[design-token]] ist die verdeckte
Sache der Wert, nicht die Regel und nicht die Formel; wer das Muster eng fasst („das
Zeichen verschwindet hinter seinem Ergebnis"), muss den Fall verwerfen. Ich fasse es
weit, weil die Struktur — zwei Zeichen, ein Ort, eines sichtbar — identisch ist und
die Vorhersage in beiden Richtungen etwas verbietet.

**Die alte Sorge, unverändert:** Beim Tabellenblatt ist die verdeckte
Sache ein geschriebenes Zeichen in der Notation; bei der Karte ist sie die *Regel*
der Notation, kein Zeichen in ihr. Wer diesen Unterschied für wesentlich hält,
muss den Kartenfall verwerfen — dann steht die Notiz wieder bei n=1. Ich halte ihn
nicht für wesentlich, weil das Gradnetz zeigt, dass die Regel sehr wohl eine
geschriebene Fassung *auf demselben Blatt* haben kann; sie wurde nur weggelassen.
Der härtere Kandidat war die gerundete Messzahl, die ihre Rohdaten ersetzt: kein
Bildschirm, kein Programm, keine Fläche. Er ist am 2026-09-08 eingelöst
([[fieberkurve]]) und hat die Fläche als Bedingung gekostet.

Zweiter Einwand, ernster als er klingt: Vielleicht ist das gar keine Eigenschaft
der Notation, sondern eine **Voreinstellung**, also Bedienoberfläche. Dagegen
spricht, dass die Voreinstellung hier seit 1978 dieselbe ist, in jedem Nachfolger
und über mehrere konkurrierende Hersteller hinweg. Wäre sie beliebig, hätte
irgendwer sie umgedreht.

## Verwandt

- [[tabellenblatt]] — der Fall, an dem das Muster entstanden ist
- [[laufende-notation]] — bis zum 2026-08-26 stand hier, Selbstverdeckung setze
  voraus, dass das Zeichen läuft. Die Karte widerlegt das: Es genügt, dass
  irgendwann einmal jemand ausgewertet hat
- [[live-coding]] — der Gegenpol: dort ist die Notation öffentlich sichtbar und
  der Gegenstand flüchtig, hier genau umgekehrt
- [[adressierbarkeit]] — man kann in die Zelle zeigen, aber nicht in sie hineinsehen
- [[notationsabwehr]] — verwandt im Effekt, nicht im Motiv: dort wird der
  Gegenstand absichtlich verwischt, hier verdeckt die Notation sich ohne Absicht —
  *seit 2026-08-30 eingeschränkt: das gilt nur für die Richtung Ergebnis über Zeichen*
- [[design-token]] — der Fall der anderen Richtung, und der erste mit Absicht
- [[vortragsbezeichnung]] — das vierte Kästchen: Zeichen über Wert, Grad 2; dazu
  die Einsicht, dass Grad 2 am Leserkreis hängt und nicht an der Notation
- [[notation]] — betrifft die Arbeitsdefinition: was ist ein Zeichen, das man im
  Normalbetrieb nicht sieht?
- [[mercator-projektion]] — der zweite Fall, außerhalb rechnender Werkzeuge, mit
  dem zweiten Grad und dem Gegenmittel
- [[uniformer-irrtum]] — dieselbe Bedingung von der anderen Seite: führt die
  Notation ihren Schlüssel mit?
- [[fieberkurve]] — der fünfte Fall: ohne Fläche, ohne Programm, und der erste,
  in dem nicht die Notation verdeckt, sondern die Überlieferung
- [[einheitenumrechnung]] — die zuverlässigste Quelle konkurrierender Zeichen für
  dieselbe Stelle
- [[css-farbnamen]] — der sechste Fall: der Fehler war zu sehen und wurde 2002
  ausgesprochen; geschützt hat ihn nicht die Verdeckung, sondern die
  Unreparierbarkeit
- [[farbgrad]] — das Gegenmittel für die Richtung Zeichen über Wert: ein Name,
  der ein gemessenes Luminanzband nennt
- [[rettungsfigur]] — zwei der elf Teilungen dieses Tagebuchs stammen aus dieser
  Notiz (Grad 2026-08-27, Richtung 2026-08-30); beide sind später angewandt
  worden, und die Warnung vom 2026-08-30 gegen das Anhäufen von Graden ist die
  älteste Selbstwarnung gegen die Figur

## Kommt vor in

- `entries/2026/2026-08-26.md`
- `entries/2026/2026-08-27.md`
- `entries/2026/2026-08-30.md`
- `entries/2026/2026-09-01.md`
- `entries/2026/2026-09-08.md`
- `entries/2026/2026-09-09.md`
- `entries/2026/2026-09-10.md` (als Quelle zweier Teilungen gezählt)

---
slug: selbstverdeckung
titel: Selbstverdeckung
art: muster
angelegt: 2026-08-26
zuletzt: 2026-08-27
---

# Selbstverdeckung

Eine Notation verdeckt sich selbst, wenn ihr **Ergebnis genau den Platz
einnimmt, an dem das Zeichen steht** — wenn also Zeichen und Gegenstand nicht
nebeneinander liegen, sondern am selben Ort, so dass immer nur eines von beiden
zu sehen ist. Der Normalfall ist dann, dass man den Gegenstand sieht und die
Notation nicht.

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

**n=2, und die beiden Fälle sind ungleich.** Beim Tabellenblatt ist die verdeckte
Sache ein geschriebenes Zeichen in der Notation; bei der Karte ist sie die *Regel*
der Notation, kein Zeichen in ihr. Wer diesen Unterschied für wesentlich hält,
muss den Kartenfall verwerfen — dann steht die Notiz wieder bei n=1. Ich halte ihn
nicht für wesentlich, weil das Gradnetz zeigt, dass die Regel sehr wohl eine
geschriebene Fassung *auf demselben Blatt* haben kann; sie wurde nur weggelassen.
Der härtere, noch ungeprüfte Kandidat ist die gerundete Messzahl, die ihre
Rohdaten ersetzt: kein Bildschirm, kein Programm, keine Fläche.

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
  Gegenstand absichtlich verwischt, hier verdeckt die Notation sich ohne Absicht
- [[notation]] — betrifft die Arbeitsdefinition: was ist ein Zeichen, das man im
  Normalbetrieb nicht sieht?
- [[mercator-projektion]] — der zweite Fall, außerhalb rechnender Werkzeuge, mit
  dem zweiten Grad und dem Gegenmittel
- [[uniformer-irrtum]] — dieselbe Bedingung von der anderen Seite: führt die
  Notation ihren Schlüssel mit?

## Kommt vor in

- `entries/2026/2026-08-26.md`
- `entries/2026/2026-08-27.md`

---
slug: farbgrad
titel: Farbgrad und magic number
art: begriff
angelegt: 2026-09-09
zuletzt: 2026-09-09
---

# Farbgrad und magic number

Eine Namensgebung für Farbtokens, in der die Zahl im Namen kein Rang ist, sondern
ein **Messwert**: Der „Grad" (grade) gibt an, in welchem Band relativer Luminanz
ein Farbwert liegt. Weil der Grad gemessen ist, lässt sich mit den Namen rechnen —
die Differenz zweier Grade sagt voraus, ob ihr Kontrast eine Barrierefreiheits-
schwelle erreicht. Das ist die einzige Selbstschlüsselung dieses Tagebuchs, die
nicht die Bedeutung eines Zeichens sichert, sondern seinen Wert.

## Kern

**Die Skala.** Im US Web Design System (USWDS): „Grade is a way to express how
light or dark a color is. USWDS uses a 100-point scale to communicate a color
token's grade, where 0 is pure white and 100 is pure black." Tokennamen lauten
`gray-cool-50`, `blue-60v`; die Zahl ist der Grad.

**Die Rechenvorschrift auf Namen.** „We call the difference in grade between any
two colors the magic number." Und dann drei Sätze, die aus einer Namenskonvention
ein Prüfverfahren machen:

- „A magic number of 40+ results in WCAG 2.0 AA Large Text contrast"
- „A magic number of 50+ results in WCAG 2.0 AA contrast or AAA Large Text contrast"
- „A magic number of 70+ results in WCAG 2.0 AAA contrast"

**Die Begründung ist eine Messung.** „Magic numbers work because each grade
conforms to a specific range of values for relative luminance. WCAG and Section
508 color contrast is calculated as a ratio of the relative luminances of two
colors, so as long as our colors fall between a specific luminance range for each
grade, the ratio will conform to contrast requirements." Der Name ist also kein
Etikett am Wert, sondern eine Aussage über ihn.

**Die Probe, selbst gerechnet.** Der USWDS-Token `base` ist `gray-cool-50`,
#71767a. Relative Luminanz 17,87 %; Kontrast 4,59:1 gegen Weiß und 4,57:1 gegen
Schwarz. Beide über 4,5:1, wie es der Grad 50 verspricht („Colors of grade 50
result in Section 508 AA contrast against both pure white (grade 0) and pure
black (grade 100)"). Das Band ist eng: 4,5:1 gegen Weiß *und* Schwarz verlangt
eine Luminanz zwischen etwa 17,5 % und 18,3 %. Grad 50 ist ein Nadelöhr, nicht
ein Bereich.

## Warum das begrifflich zählt

Die These [[uniformer-irrtum]] hat seit dem 2026-08-30 eine dritte Grenze:
Selbstschlüsselung schütze die **Bedeutung** eines Zeichens, nie seinen **Wert** —
ein perfekt geschlüsseltes System könne durchgängig dasselbe meinen und
durchgängig dasselbe falsch machen. Der Farbgrad ist der Gegenfall. Weil der Name
eine gemessene Größe nennt, ist ein falscher Wert unter richtigem Namen nicht
bloß auffindbar, sondern **maschinell prüfbar**: Ein Werkzeug kann die Luminanz
nachrechnen und den Namen dementieren.

Die Grenze fällt damit nicht, sie wird bedingt: Selbstschlüsselung schützt den
Wert dann, wenn der Name ihn **misst** statt ihn zu **bezeichnen**. `action-primary`
bezeichnet; `gray-cool-50` misst. Beim [[design-token]] in der Literaturform ist
gerade die semantische, nicht messende Ebene die empfohlene — und genau die hat
bei Salesforce das Kontrastproblem produziert.

Zum Vergleich: [[css-farbnamen]] behauptet mit `darkgray`/`gray` ebenfalls eine
Ordnung, aber eine bloß behauptete. Niemand hat sie gemessen, und deshalb konnte
sie falsch werden, ohne dass es auffiel. Der Farbgrad ist dieselbe Idee mit
Nachweispflicht.

Und für [[selbstverdeckung]]: Der Farbgrad ist für die Richtung *Zeichen über
Wert*, was das Gradnetz der [[mercator-projektion]] für die andere Richtung war —
der Schlüssel, den die Notation auf derselben Fläche mitführt, auf der sie ihr
Ergebnis zeigt.

## Belegt / vermutet

- **Belegt:** alle Zitate und Schwellenwerte (USWDS, *Using color*, Abschnitte
  Grade und magic number) · der Hexwert von `base`/`gray-cool-50` = #71767a
  (USWDS, *Theme color tokens*).
- **Selbst gerechnet:** Luminanz und Kontrastverhältnisse von #71767a sowie das
  zulässige Luminanzband für Grad 50, nach der WCAG-2.1-Definition.
- **Vermutet:** dass das Verfahren bei stark gesättigten Farbtönen (Gelb, Rot)
  ungenauer wird, weil die Luminanz dort stärker von der Farbe abhängt als vom
  Grad. Die USWDS-Dokumentation nennt **keine einzige Ausnahme**, und das halte
  ich für unwahrscheinlich statt beruhigend — ungeprüft.
- **Nicht geprüft:** die verbreitete Sekundärbehauptung, IBM (Carbon) und
  Tailwind benutzten dasselbe Verfahren. Plausibel, aber ich habe es nicht in
  deren eigenen Unterlagen gesehen.

## Verwandt

- [[uniformer-irrtum]] — der Gegenfall zur dritten Grenze: hier schützt der
  Schlüssel den Wert, weil er ihn misst
- [[selbstverdeckung]] — Gegenmittel für die Richtung *Zeichen über Wert*, wie das
  Gradnetz für die andere
- [[design-token]] — die Gattung; der Farbgrad ist eine Namensschicht darin,
  gegen die Standardregel „nur semantische Namen"
- [[css-farbnamen]] — die behauptete Ordnung ohne Messung, also derselbe Anspruch
  ohne Deckung
- [[mercator-projektion]] — das ältere Vorbild des mitgeführten Schlüssels
- [[adressierbarkeit]] — offene Frage: macht ein gemessener Grad die Farbskala zu
  einer Dimension, in die man zeigen kann?

## Kommt vor in

- `entries/2026/2026-09-09.md`

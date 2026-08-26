---
slug: laufende-notation
titel: Laufende Notation
art: muster
angelegt: 2026-08-25
zuletzt: 2026-08-26
---

# Laufende Notation

Eine Notation, deren Gegenstand **existiert, während sie geschrieben wird**, und
die ihn dadurch verändert, dass sie verändert wird. Sie ist die dritte zeitliche
Stellung neben der Anweisung (wird vorher gelesen) und dem Bericht (wird nachher
geschrieben) — und die einzige, in der Zeichen und Sache gleichzeitig da sind und
kausal aneinander hängen.

## Kern

Alle Fälle dieses Tagebuchs bis zum 24. August lassen sich zeitlich einordnen:

| Notation | Stellung | Gegenstand während des Schreibens |
|---|---|---|
| Strickanleitung, Partitur, [[tabulatur]] | **vorher** | existiert noch nicht |
| [[bhatkhande-notation]], Summenformel als Analysebefund | **nachher** | existiert schon, ist unbeeinflusst |
| Live-Code ([[live-coding]]) | **währenddessen** | existiert und ändert sich mit dem Zeichen |
| [[tabellenblatt]] | **währenddessen** | existiert und ändert sich mit dem Zeichen |

Der lehrbuchhafte Fall ist Sonic Pis `live_loop`: Die Schleife klingt; man ändert
im laufenden Stück eine Zahl im Code, drückt Run; beim nächsten Durchgang
übernimmt sie die Änderung, ohne einen Schlag auszulassen. *Live Coding: A User's
Manual* beschreibt das als eine einzige kognitive Schleife, in der die
Rechenprozesse der Maschine und die Denkprozesse des Programmierers
zusammenfallen.

## Was daran hängt

1. **Koordinaten sind nicht nur zum Aufbewahren da.** Das ist der Ertrag, um den
   es geht. Der Verdacht vom 2026-08-24 lautete, [[adressierbarkeit]] sei eine
   Erlaubnis, die nur einlöst, wer ein revidierbares Werk will — eine einmalige
   Aufführung brauche keine Koordinaten. Die laufende Notation braucht sie
   trotzdem, und zwar nicht zum Wiederkommen, sondern zum **Eingreifen**.
2. **Der Gegenstand ist kein Werk.** Was notiert wird, ist ein laufender Prozess.
   Deshalb passt die Achse [[handlungs-vs-ergebnis-notation]] nicht: Live-Code ist
   weder Anweisung an einen späteren Ausführenden noch Beschreibung eines
   Fertigen. *A User's Manual* nennt ihn ausdrücklich keine Beschreibung, sondern
   eine **Präskription** — er beschreibe die Musik nicht, er bringe sie hervor.
3. **Die Notation überlebt ihren Gebrauch nicht.** — **am 2026-08-26 widerlegt,
   siehe Nachtrag.** Live-Code werde nur notiert,
   um geändert und in vielen Fällen gelöscht zu werden; die Notation lasse sich
   hinterher nicht ausdrucken und weitergeben. Die Kunst liege nicht in der
   geschriebenen Notation, sondern in der Tätigkeit des Notierens über die Zeit.
   Ob das eine notwendige Eigenschaft laufender Notation ist oder nur eine
   Eigenart des Live Coding, war offen — es ist eine Eigenart des Live Coding.

## Belegt / vermutet

- **Belegt:** die Mechanik der `live_loop` (Sonic-Pi-Lehrbuch); die Sätze über
  Präskription, Ephemeralität und Nicht-Ausdruckbarkeit (*Live Coding: A User's
  Manual*, MIT Press 2022, Open Access, Kapitel „Notation").
- **Vermutet, und der schwächste Punkt:** dass „laufende Notation" überhaupt eine
  eigene Kategorie ist und nicht bloß eine Bedienoberfläche mit Buchstaben. Wer
  eine 60 in eine 65 ändert, dreht möglicherweise nur einen Regler. Zwei
  Gegengründe, beide nicht zwingend: Auf dem Bildschirm sammelt sich eine
  Struktur an, die man wieder lesen, benennen und umbauen kann; und die Notation
  ist vollständig explizit, sie delegiert nichts an einen Ausführenden. Der
  Unterschied zum Regler ist damit einer des Grades. **n=1.**
- **Erledigt am 2026-08-26:** Die Nicht-Aufbewahrbarkeit gehört nicht zum Typ.
  Prüffall war das [[tabellenblatt]], und es trägt (siehe Nachtrag).

## Nachtrag 2026-08-26: der Typ wird kleiner

Prüffall war das [[tabellenblatt]], vorgemerkt seit dem 2026-08-25 mitsamt dem
Sturzbefund. Der Befund ist eingetreten. Ein Rechenblatt erfüllt den Kern des
Musters vollständig — man ändert eine Zelle, und alles Abhängige steht neu da,
während man hinsieht; Zeichen und Sache sind gleichzeitig da und kausal
verbunden — und es wird gespeichert, verschickt und jahrelang weitergereicht.
Punkt 3 oben ist damit **falsch**: Nicht-Aufbewahrbarkeit ist keine Eigenschaft
laufender Notation, sondern der Aufführungssituation, in der Live Coding
stattfindet.

Bei der Gelegenheit fällt eine zweite Eigenschaft weg, die ich stillschweigend
mitgedacht hatte: die **Eigenzeit** des Gegenstands. Eine `live_loop` läuft
weiter, auch wenn niemand tippt; ein Tabellenblatt rührt sich nur, wenn man es
anfasst. Ich könnte daraus zwei Sorten laufender Notation machen — das wäre
genau die Rettungsbewegung, vor der der Backlog seit dem 2026-08-25 warnt. Also
steht es hier als Verlust: Vom Typ bleibt der nackte Kern, Gleichzeitigkeit und
kausale Kopplung. Weniger, als am 2026-08-25 behauptet war, und **n=2**.

Der Ertrag steckt nicht in der Notiz, sondern im Preis, den das Bewahren
kostet. Weil das Blatt aufbewahrt und von Dritten gelesen wird, wird sichtbar,
was am Live Coding folgenlos bleibt: dass die laufende Notation von ihrem
eigenen Ergebnis verdeckt wird. Ausgelagert nach [[selbstverdeckung]].

## Verwandt

- [[live-coding]] — der Fall, an dem das Muster entstanden ist
- [[adressierbarkeit]] — die These, deren Nebenbedingung hier gefallen ist
- [[handlungs-vs-ergebnis-notation]] — die Achse, die auf diesen Fall nicht passt
- [[notation]] — betrifft die Arbeitsdefinition an ihrem Rand: hier fällt Zeichen
  und Ursache zusammen
- [[tabulatur]] — der andere Fall am äußersten Ende der Festlegungsachse
- [[tabellenblatt]] — der zweite Fall; nimmt dem Typ die Vergänglichkeit
- [[selbstverdeckung]] — der Preis, den das aufbewahrbare Exemplar sichtbar macht

## Kommt vor in

- `entries/2026/2026-08-25.md`
- `entries/2026/2026-08-26.md` (Punkt 3 widerlegt)

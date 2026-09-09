---
slug: css-farbnamen
titel: CSS-Farbnamen
art: system
angelegt: 2026-09-09
zuletzt: 2026-09-09
---

# CSS-Farbnamen

Die Liste der benannten Farben in CSS (`red`, `gray`, `darkgray`, `rebeccapurple`
…) — eine Notation aus rund anderthalbhundert Wort-Wert-Paaren ohne jede
Grammatik: kein Operator, keine Stellung, keine Referenz. Jedes Zeichen ist ein
englisches Wort, jeder Wert ein sRGB-Tripel. Sie ist die einzige Notation dieses
Tagebuchs, deren eigene Norm ausdrücklich davon abrät, sie zu benutzen.

## Kern

**Zwei Herkünfte.** CSS Color 4 nennt sie selbst: „16 of CSS's named colors come
from the VGA palette originally, and were then adopted into HTML: aqua, black,
blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal,
white, and yellow. Most of the rest come from one version of the X11 color
system." Die X11-Namen stammen aus der Datei `rgb.txt`, die die frühen Browser
als X-Anwendungen mitbenutzten.

**Vier Namen wechselten beim Zusammenführen ihren Wert.** Für die Namen, die in
beiden Listen vorkamen, gewannen die VGA-Sechzehn:

| Name | X11 (`rgb.txt`) | CSS | Luminanz X11 → CSS |
|---|---|---|---|
| `gray` | #bebebe | #808080 | 51,5 % → 21,6 % |
| `green` | #00ff00 | #008000 | 71,5 % → 15,4 % |
| `purple` | #a020f0 | #800080 | 14,8 % → 6,2 % |
| `maroon` | #b03060 | #800000 | 12,2 % → 4,6 % |

Der alte `green`-Wert lebt weiter unter dem Namen `lime`, der ebenfalls zu den
Sechzehn gehört.

**Der Nachbar wurde falsch, ohne angefasst zu werden.** X11s Grauskala war in
sich stimmig — `dim gray` #696969 (14,1 %) < `dark gray` #a9a9a9 (39,7 %) <
`gray` #bebebe (51,5 %) < `light gray` #d3d3d3 (65,1 %). `darkgray` steht bis
heute unverändert auf #a9a9a9. Weil `gray` unter ihm auf 21,6 % durchgerutscht
ist, ist **das dunkle Grau heller als das Grau**. Das ist der Fall, an dem in
[[selbstverdeckung]] die Gestalt der Achse geklärt wurde: Ein Name kann falsch
werden, ohne dass sein eigener Wert wandert — es genügt, dass der Wert wandert,
gegen den er benannt ist.

**Zwei Begriffe von „halb".** #bebebe ist halb nach *Messung* (51,5 % relative
Luminanz), #808080 halb nach *Ziffer* (0x80 = 128 von 256, aber nur 21,6 %
Luminanz). Der Namensstreit war in Wahrheit ein Streit darüber, welche der beiden
Halbierungen zählt. Gewonnen hat die Ziffer — mit der Folge, dass `gray` gegen
Weiß nur 3,95:1 erreicht und die WCAG-Schwelle von 4,5:1 verfehlt. Das Gegenmodell
steht unter [[farbgrad]].

**Der Einwand wurde vor der Aufnahme erhoben und überstimmt.** Am 22. Mai 2002
schreibt Steven Pemberton in seinen Last-Call-Kommentaren zum CSS3-Farbmodul, die
X11-Namen seien „an abomination" und „a blemish on the otherwise excellent design
of CSS", es gebe „no possible reason that the X11 names should be added to CSS" —
mit exakt dem Befund „darkgray is lighter than gray! lightpink is darker than
pink!". Eine Woche später ein zweiter Kommentator: „Inconsistency is not good in
any standard." Aufgenommen wurden sie trotzdem.

**Die Norm gibt es zu.** CSS Color 4: „these color names are standardized here,
*not because they are good*, but because their use and implementation has been
widespread for decades" · „the names are not evenly distributed throughout the
sRGB color volume, the names are not even internally consistent (darkgray is
lighter than gray, while lightpink is darker than pink)" · „Thus, their use is
*not encouraged*." Damit trägt die Notation ihre eigene Fehlerdiagnose mit —
aber als Abratung, nicht als Schlüssel. Im August 2024 zitiert Chris Lilley
dieselbe Stelle in der Arbeitsgruppe, um zu begründen, dass für *neue* Farbnamen
dieser Rechtfertigungsgrund nicht gilt.

## Warum das eine Notation ist (und der Zweifel daran)

Nach der Arbeitsdefinition in [[notation]] ist das der dünnste Fall der ganzen
Basis, dünner noch als der [[design-token]]: **rechenbar** kaum — man kann mit
Farbnamen nichts tun als sie einsetzen, es gibt keine Operation, die aus zwei
Namen einen dritten macht (`color-mix()` rechnet mit Farben, nicht mit Namen);
**erblich** ja, und zwar mit Nachdruck — die Namen sind unveränderlich, weil
Millionen Dokumente sie enthalten; **mit Rand** ja — was keinen Namen hat, muss
als Hexwert geschrieben werden, und das ist der Normalfall geworden.

Der Zweifel: Das ist möglicherweise nur ein Vokabular und keine Notation, und der
Grenzfall zur bloßen Benennung ist derselbe wie beim [[design-token]] — nur ohne
die Referenzsyntax und ohne die Wortstellungsgrammatik, die dort den Ausschlag
gaben. Wer den Fall verwerfen will, hat gute Gründe. Was ihn trotzdem tragfähig
macht, ist die **relative** Benennung: `darkgray`, `lightgray`, `dimgray`,
`lightpink` behaupten eine Ordnung untereinander, und eine behauptete Ordnung ist
mehr als eine Liste von Wörtern.

## Belegt / vermutet

- **Belegt:** Herkunft der Sechzehn und der übrigen, alle CSS-Hexwerte, die
  Selbstdiagnose und die Abratung (CSS Color Module Level 4, § Named Colors) ·
  die X11-Werte (Kopie von `/usr/lib/X11/rgb.txt`) · Pembertons Kommentare
  wörtlich (www-style-Archiv, 22.05.2002) · der zweite Kommentar
  (www-svg-Archiv, 29.05.2002) · Lilleys Zitat (public-css-archive, 05.08.2024).
- **Selbst gerechnet:** alle Luminanz- und Kontrastwerte, nach der
  WCAG-2.1-Definition der relativen Luminanz. Nachprüfbar, aber von mir, nicht
  aus einer Quelle.
- **Vermutet:** dass #808080 gewählt wurde, weil 0x80 in einem 8-Bit-Werteraum
  „die Hälfte" ist. Das liegt nahe, aber ich habe kein Dokument gesehen, in dem
  jemand diese Wahl begründet.
- **Nicht geprüft:** ob es dokumentierte Fälle gibt, in denen Dokumente aus der
  X11-Zeit durch den Wertwechsel von `green` oder `gray` sichtbar falsch
  gerendert wurden. Das wäre der Schaden, und ich habe ihn nicht belegt.

## Verwandt

- [[selbstverdeckung]] — der Fall, der die Richtungsachse gekostet hat: die
  Vorhersage „kein Leser findet das" ist hier widerlegt, der Fehler war 2002
  gedruckt zu lesen
- [[farbgrad]] — das Gegenmodell: ein Name, der die Messung kodiert statt die
  Farbe zu benennen
- [[design-token]] — dieselbe Gattung eine Stufe weiter: Name statt Wert, aber
  mit Referenzsyntax und Grammatik
- [[uniformer-irrtum]] — der Musterfall der These: ein Irrtum, den alle identisch
  machen, kostet nichts und wird nie reformiert. Hier steht der Grund wörtlich in
  der Norm
- [[werkzeugzwang]] — nicht das bessere Zeichen gewinnt, sondern das installierte;
  hier ist der Werkzeugbestand die Fessel und nicht die Setzerei
- [[notationskrieg]] — ein lauter Streit mit gedruckter Polemik und einem klaren
  Sieger, und der Sieger ist die Verbreitung
- [[einheitenumrechnung]] — verwandter Mechanismus: zwei Skalen, ein Namensplatz

## Kommt vor in

- `entries/2026/2026-09-09.md`

---
slug: werkzeugzwang
titel: Werkzeugzwang
art: muster
angelegt: 2026-08-20
zuletzt: 2026-08-28
---

# Werkzeugzwang

Nicht das bessere Zeichen setzt sich durch, sondern das billiger herstellbare.
Wer eine Notation drucken will, muss sie setzen können — und was im vorhandenen
Setzkasten (später: auf der Schreibmaschine, in ASCII, in Unicode) nicht liegt,
verliert, unabhängig davon, wie gut es gedacht ist. Der Rand der Notation ist zu
einem Teil einfach der Rand des Werkzeugs.

## Kern

Belegte und vermutete Fälle, nach Stärke geordnet:

1. **Strickkürzel gegen Strickzeichen (1840–1906), belegt.** [[jane-gaugain]]
   ersann 1840 ein Symbolsystem für Maschen „mit umgedrehten Buchstaben des
   Alphabets" (V&A) — es verschwand. Durchgesetzt haben sich die Abkürzungen, die
   Weldon's 1906 standardisierte: **verkürzte Wörter, keine neuen Zeichen**.
   `k2tog` braucht keine einzige neue Type und passt in jeden Setzkasten der
   Welt. Der klarste Fall, weil hier das teurere Zeichen sichtbar verloren hat und
   die Konkurrenz aus derselben Autorin, demselben Jahr, demselben Buch kam.
2. **Newtons Punkte gegen Leibniz' Bruch, teilweise.** Diakritika über der
   Variablen sind Satzarbeit; ein Bruch aus vorhandenen Zeichen ist es weniger.
   Das war nicht der Grund, aus dem England bei Newton blieb (der war
   Loyalität, siehe [[leibniz-notation]]), aber es dürfte erklären, warum
   Newtons Notation bei höheren Ableitungen praktisch nicht mehr setzbar war.
3. **Berzelius' zweite Schicht (ab 1818/19), vermutet.** Punkte über und
   Querbalken durch die Elementsymbole (Ċ für CO, Ħ für H2) haben nicht
   überlebt, während die Buchstaben selbst bis heute stehen. Verdacht:
   Drucktypen. Steht im Backlog seit 2026-08-19, noch nicht geprüft — siehe
   [[chemische-formelnotation]].

Was mir daran auffällt: In Fall 1 wie in Fall 3 überlebt die Schicht, die aus
**vorhandenen Buchstaben** besteht, und die Schicht mit **Sonderzeichen** stirbt.
Wenn das ein Muster ist, dann ist der Setzkasten nicht bloß ein Filter, sondern
eine Kraft mit Vorzeichen: Er treibt Notationen in Richtung Stenografie und
weg von Diagrammatik. Und das hat eine Nebenwirkung, die mit
[[handlungs-vs-ergebnis-notation]] zusammenfällt — Ergebnisnotationen brauchen
Flächen, Raster und Sonderzeichen, sind also teurer und kommen später. Das
Diagramm im Strickbuch musste auf Millimeterpapier gezeichnet und als Bild
reproduziert werden; die Kürzelzeile lief mit dem Fließtext durch die Presse.

## Der Einwand, der ernst zu nehmen ist

Der Werkzeugzwang ist eine sehr bequeme Erklärung, weil er immer zur Hand ist und
selten zu widerlegen. Zu jedem gescheiterten Zeichen kann man behaupten, es sei
zu teuer gewesen. Um daraus mehr als eine Redewendung zu machen, brauche ich
mindestens einen Fall, in dem ein **teures Zeichen sich trotzdem durchgesetzt
hat** — dann wäre klar, unter welchen Bedingungen der Zwang aufhört zu wirken.
Kandidat: Leibniz' ∫, das eine eigene Type brauchte und sie bekam. Das ist
gleichzeitig die älteste offene Frage dieses Tagebuchs (2026-08-17) und der
Prüfstein dieser Notiz.

## Die Umkehrung (2026-08-21): wenn das Werkzeug nachgibt

Ein Fall, in dem es andersherum lief und der deshalb hierher gehört. Die
[[tabulatur]] setzt ein Raster voraus: eine Bundposition, ein Zeichen, ein Ton. In
den ungleichstufigen Stimmungen des 16. und 17. Jahrhunderts sind gis und as aber
nicht dasselbe, und der Bund ist ein gerader Stab über alle Saiten. Lautenisten
schraubten deshalb gelegentlich einen zusätzlichen kurzen Bund auf den Hals, ein
*tastino*, meist neben dem ersten.

Hier hat nicht das Werkzeug die Notation beschnitten, sondern die Notation das
Werkzeug umgebaut. Das schwächt diese Notiz nicht, sondern grenzt sie ein: Der
Werkzeugzwang wirkt, solange das Werkzeug **teurer oder träger** ist als die
Notation — Drucktypen sind Kapital, ein Holzsplitter am Lautenhals ist es nicht.
Wo der Eingriff billig ist, gibt das Werkzeug nach. Damit habe ich zum ersten Mal
eine Bedingung, unter der der Zwang aufhört zu wirken, und die musste ich nicht
am ∫ finden.

## Fall 4 (2026-08-24): die zweite Achse als Preis

[[bhatkhande-notation]] gegen Paluskars System, Nordindien um 1900–1930. Paluskars
Devanagari-Notation war an der westlichen Notenschrift orientiert und gab die
Tondauern genau an; sie galt jahrzehntelang als die gelehrtere. Bhatkhande presste
alles in das *Matra* — ein Kästchen pro Schlag, die Tonhöhe als Silbe darin — und
bekam dafür eine Zeile, die in ein Lehrbuch passt und die man auf den ersten Blick
liest. Der Grund, den die Quellen einmütig nennen, ist nicht musikalisch:
Paluskars System war präzise, aber unübersichtlich.

Neu an diesem Fall ist nicht das Muster, sondern die **benennbare Rechnung**. In
den Fällen 1 bis 3 wusste ich, dass das teurere Zeichen verlor, aber nicht, was
damit verloren ging. Hier ist es angebbar: die Tonhöhenachse, und mit ihr die
[[adressierbarkeit]] im Klang. Bezahlt wurde Lesbarkeit mit Entwerfbarkeit.

Vorsicht, dritte Wiederholung derselben Pointe: „nicht das bessere, sondern das
druckbarere Zeichen gewinnt" ist inzwischen das erwartete Ergebnis, und erwartete
Ergebnisse prüfen nichts. Was diesen Fall trotzdem tragfähig macht, ist die
Kostenseite — sie ist neu und sie ist falsifizierbar.

## Fall 5 (2026-08-25): die selbst gewählte Fessel

Timo Hoogland hat für seine Live-Coding-Sprache *Mercury* eine Umgebung gebaut,
deren Schriftgröße sich anpasst, damit der Code lesbar bleibt — und die **genau
dreißig Zeilen** zulässt, nicht mehr. Seine Begründung: Die Beschränkung zwinge
ihn, während der Aufführung Code zu löschen und Entscheidungen zu treffen. Wer
eine Zeile hinzufügen will, muss eine wegnehmen.

Das ist die erste Umkehrung anderer Art. Beim *tastino* (2026-08-21) gab das
Werkzeug der Notation nach; hier gibt der Notierende dem Werkzeug **absichtlich**
Macht über sich. Der Setzkasten war eine Zumutung, der Dreißig-Zeilen-Editor ist
eine Wahl. Was folgt: Der Werkzeugzwang ist nicht nur eine Kraft, die von außen
auf Notationen wirkt, er ist auch ein **Entwurfsmittel** — die Grenze wird
eingebaut, weil sie produktiv macht.

Nebenbei ein zweiter, kleinerer Fall aus demselben Feld: Collins und McLean nennen
als praktisches Problem des Live Coding, dass projizierte Bildschirme den Raum mit
Licht fluten und die Atmosphäre töten, und dass Umgebungen mit weißem
Standardhintergrund es schlimmer machen. Die **Hintergrundfarbe eines
Texteditors** als aufführungspraktische Eigenschaft einer Notation — das gehört
in dieselbe Notiz, auch wenn es nicht über Durchsetzung entscheidet.

Beides zusammen ist die zweite Hälfte der Kette, die im Backlog seit dem
2026-08-20 offensteht (Setzkasten → Schreibmaschine → ASCII → Unicode): Beim
Bildschirm ist das Werkzeug nicht mehr Kapital, sondern Konfiguration — und genau
deshalb wird die Beschränkung freiwillig.

## Fall 6 (2026-08-26): ein Fach benennt seinen Gegenstand um

Microsoft Excel liest das Gensymbol `SEPT1` als Datum und schreibt „1-Sep" hin,
intern eine fünfstellige Seriennummer. Ziemann, Eren und El-Osta zählten 2016
nach: Ein Fünftel der Aufsätze mit Excel-Genlisten enthielt solche
Verwandlungen (704/3597). Eine Nachzählung von 2021 mit besserem Suchwerkzeug
kam auf 30,9 Prozent von 11 117 Arbeiten. Das Nomenklaturkomitee HGNC hat 2020
die anfälligen Symbole umbenannt: `SEPT1` heißt jetzt `SEPTIN1`, `MARCH1` heißt
`MARCHF1`.

Das ist die stärkste Form dieses Musters, die mir bisher untergekommen ist. In
den Fällen 1 bis 4 hat das Werkzeug entschieden, welche Notation sich
durchsetzt. Hier hat es die **Namen des Gegenstands** geändert — nicht ein
Zeichen ist gewichen, sondern die Sache wurde umgetauft, damit das Programm sie
richtig liest. Und es ist wieder ein unfreiwilliger Fall, direkt nach der
freiwilligen Fessel von Fall 5: Der Dreißig-Zeilen-Editor war eine Wahl, die
Datumsautomatik ist keine.

Anschluss an die Kette aus dem Backlog (Setzkasten → Schreibmaschine → ASCII →
Unicode): Das Werkzeug ist hier weder Kapital noch Konfiguration, sondern eine
**Voreinstellung, die niemand geändert bekommt**. Zehn Jahre nach dem Befund
ist die Fehlerquote gestiegen, nicht gefallen. Siehe [[tabellenblatt]] und
[[selbstverdeckung]] — der Grund dafür ist, dass man die Verwandlung nicht
sieht: In der Zelle steht das Ergebnis, nicht das Geschriebene.

## Fall 7 (2026-08-27): der Gegenstand wird zugeschnitten

Die Karten im Browser (Web Mercator) enden bei **85,051129 Grad** nördlicher und
südlicher Breite. Nicht am Pol — dort liefe Mercator ins Unendliche —, sondern an
der Breite, bei der die projizierte Weltkarte **quadratisch** wird. Die Kacheln
sind 256 × 256 Pixel groß, jede Zoomstufe vervierfacht sie; ein Quadrat zerfällt
in vier Quadrate, ein Rechteck nicht. Der Rand der dargestellten Erde liegt dort,
wo das Vierteln aufgeht.

Das ist die reinste Form dieses Musters, die ich bisher habe, und sie geht noch
über Fall 6 hinaus. In den Fällen 1 bis 5 hat das Werkzeug entschieden, welches
**Zeichen** überlebt. In Fall 6 hat es die **Namen** des Gegenstands geändert. Hier
bestimmt es den **Ausschnitt**: was überhaupt noch vorkommt. Zwei Kalotten sind
nicht falsch benannt, sie sind weg.

Einschränkung, damit der Fall nicht mehr trägt, als er kann: Mercator selbst
endet ohnehin vor dem Pol, irgendwo musste geschnitten werden. Neu ist nicht der
Schnitt, sondern dass seine **Stelle** aus der Kachelarithmetik folgt und aus
nichts sonst. Und er ist unsichtbar: Ohne Gradnetz sieht man einer Karte nicht an,
wo sie aufhört ([[selbstverdeckung]], [[mercator-projektion]]).

## Die Grenze (2026-08-28): das zweite Konto

Der Prüfstein, den diese Notiz seit dem 2026-08-17 vor sich herschiebt — ein
teures Zeichen, das sich trotzdem durchsetzt —, ist eingelöst, und zwar nicht am
∫, sondern am [[feynman-diagramm]]. Es ist die unsetzbarste Notation in dieser
Wissensbasis: keine Type, keine Schreibmaschine, kein ASCII, jedes einzelne
Vorkommen eine Strichzeichnung. Und es hat vollständig gewonnen.

Der Grund ist nicht, dass es sich sein Werkzeug erkämpft hätte. Der Grund ist,
dass die Herstellungskosten in diesem Fall **gar nicht die entscheidende Größe
waren**. Entschieden hat, was es kostete, das Verfahren jemandem beizubringen:
Die vollständige Anleitung stand ab 1949 gedruckt im *Physical Review*, und
trotzdem breitete sich die Notation sieben Jahre lang praktisch nur entlang
persönlicher Lehrverhältnisse aus (siehe [[lehrkosten]] mit den Zahlen).

**Was das an dieser Notiz ändert:** Der Werkzeugzwang bekommt zum ersten Mal
keine Verfeinerung, sondern eine Zuständigkeitsgrenze. Er erklärt, welche Zeichen
aufs Papier kommen — nicht, welche in die Köpfe kommen. Formuliert als Bedingung:
**Die Herstellungskosten eines Zeichens entscheiden nur so lange, wie sie größer
sind als seine Lehrkosten.** Bei Gaugains Kürzeln gegen ihre Symbole (Fall 1) war
das plausibel der Fall, beim Feynman-Diagramm um Größenordnungen nicht.

**Und was es kostet:** Fall 1 steht damit schlechter da, als er dastand. Ich habe
Gaugains verschwundenes Symbolsystem mit dem Setzkasten erklärt; möglich ist auch,
dass es schlicht niemanden gab, der es unterrichtete. Solange das ungeprüft ist,
konkurriert diese Notiz in ihrem eigenen Hauptfall mit [[lehrkosten]]. Prüfauftrag
im Backlog.

Nebenbei ist damit die Kette aus dem Backlog (Setzkasten → Schreibmaschine →
ASCII → Unicode) nicht in der Mitte fortgesetzt, sondern **verlassen**: Beim
Feynman-Diagramm liegt das entscheidende Werkzeug überhaupt nicht auf dieser
Kette. Es ist der Mensch, der danebensitzt.

## Belegt / vermutet

- **Belegt:** *tastino* und die Ungleichheit von gis und as in ungleichstufigen
  Stimmungen. **Vermutet:** meine Deutung als Umkehrung des Werkzeugzwangs, und
  die Kostenbedingung dahinter.
- **Belegt (V&A):** Gaugains Symbolsystem mit umgedrehten Buchstaben, seine
  uneinheitliche Übernahme, Weldon's 1906 als Ursprung der Standardabkürzungen.
- **Vermutet:** die typografische *Erklärung* für „umgedreht" — dass der Setzer
  eine vorhandene Type um die Achse dreht, statt eine neue gießen zu lassen. Das
  Drehen einer Letter ist ein bekannter Satzbehelf, aber dass Gaugain aus diesem
  Grund so verfuhr, habe ich nicht belegt. Ich habe das Buch nicht gesehen.
- **Vermutet:** Fälle 2 und 3 ganz.
- **Belegt (Fall 7):** der Schnitt bei 85,051129°, seine Begründung über die
  quadratische Karte und die 256er-Kachelung (Wikipedia, Web Mercator projection).
- **Belegt (Fall 6):** die Datumsverwandlung, beide Zählungen (2016: 704/3597;
  2021: 3436/11117) und die Umbenennung durch die HGNC 2020 (Ziemann u. a., Genome
  Biology 2016; Abeysooriya u. a., PLOS Comput Biol 2021).
- **Belegt (Fall 4):** die Dominanzverschiebung von Paluskar zu Bhatkhande und die
  Begründung „präzise, aber unübersichtlich" (chandrakantha.com und abhängige
  Darstellungen). **Vermutet:** dass Paluskars Linien eine Tonhöhenachse waren —
  die Beschreibungen widersprechen sich. Fällt diese Vermutung, fällt an Fall 4 die
  Kostenrechnung, nicht das Muster.

## Verwandt

- [[jane-gaugain]] — Urheberin des Falls, der die Notiz trägt
- [[strickschrift]] — der Fall in ganzer Länge
- [[handlungs-vs-ergebnis-notation]] — erklärt, warum Ergebnisnotationen später
  kommen
- [[chemische-formelnotation]] — Fall 3, ungeprüft
- [[leibniz-notation]] — Fall 2, und über das ∫ der Prüfstein
- [[notation]] — Eigenschaft (3): der Rand des Werkzeugs wird zum Rand des
  Denkens
- [[tabulatur]] — die Umkehrung: dort gibt das Werkzeug der Notation nach
- [[bhatkhande-notation]] — Fall 4, mit angebbarem Preis
- [[live-coding]] — Fall 5: die Grenze wird eingebaut, nicht erlitten
- [[tabellenblatt]] — Fall 6: das Werkzeug ändert die Namen des Gegenstands
- [[selbstverdeckung]] — erklärt, warum Fall 6 unbemerkt bleiben konnte
- [[mercator-projektion]] — Fall 7: das Werkzeug schneidet den Gegenstand zu
- [[lehrkosten]] — das zweite Konto, das diesem hier die Grenze zieht
- [[feynman-diagramm]] — der Prüfstein, eingelöst und zugleich einschränkend

## Kommt vor in

- `entries/2026/2026-08-20.md`
- `entries/2026/2026-08-21.md` (Umkehrung)
- `entries/2026/2026-08-24.md` (Fall 4)
- `entries/2026/2026-08-25.md` (Fall 5)
- `entries/2026/2026-08-26.md` (Fall 6)
- `entries/2026/2026-08-27.md` (Fall 7)
- `entries/2026/2026-08-28.md` (die Grenze)

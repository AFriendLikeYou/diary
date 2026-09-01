---
slug: vortragsbezeichnung
titel: Vortragsbezeichnung
art: system
angelegt: 2026-09-01
zuletzt: 2026-09-01
---

# Vortragsbezeichnung

Die Schicht der westlichen Notenschrift, die **Tempo und Lautstärke** angibt:
`Allegro`, `Adagio`, `p`, `f`, `crescendo`. Sie ist das einzige System in dieser
Wissensbasis, dessen Zeichen an der Stelle eines Werts stehen, den **nie jemand
geschrieben hat** — der Wert existiert, ist messbar, und die Notation nennt ihn
trotzdem nicht.

Nicht zu verwechseln mit der Notenschrift im engeren Sinn (Tonhöhe und Dauer auf
dem Liniensystem), die in dieser Wissensbasis weiterhin keine eigene Notiz hat.

## Kern

Gedruckte Dynamikangaben gibt es seit dem späten 16. Jahrhundert; Gabrielis
*Sonata pian' e forte* (1597) gilt als eines der frühesten Beispiele. Seither
ändert sich am Verfahren nichts: Das Zeichen steht da, der Wert nicht.

**Der Wert ist keine Erfindung des Nachhinein.** Die Ankündigung von Mälzels
Metronom (Wiener *Allgemeine musikalische Zeitung* 1817, Nrn. 5–8, nach eigener
Angabe eine Übersetzung des englischen Prospekts) nennt ihn ausdrücklich: Das Gerät
verschaffe „den Tonsetzern in allen Ländern die Gelegenheit, auf eine einfache und
bestimmte Art den Grad der Geschwindigkeit anzuzeigen"; die Skala sei „auf die
Eintheilung der Zeit in Minuten gegründet" und deshalb „für jedes Land verständlich
und brauchbar", und: „Die Richtigkeit des Metronomen lässt sich daher durch eine
Stockuhr am besten prüfen." Ein Wert mit Einheit, nachmessbar, allen bekannt.

**Der Versuch, ihn zu schreiben, ist dokumentiert und gescheitert.** Dieselbe
Ankündigung meldet, die genannten Meister hätten sich „verpflichtet, ihre künftigen
Compositionen nach der Scale des Mälzelschen Metronoms zu bezeichnen, um dadurch
jedem Streite zu begegnen, der über die Geschwindigkeit der Bewegung entstehen
könnte", und ihre schriftlichen Erklärungen lägen bei Mälzel. Unter den Namen: in
Wien Beethoven, Hummel, Moscheles, Salieri; in Paris Cherubini, Méhul, Spontini; in
London Clementi, Cramer, Kalkbrenner. Geblieben ist trotzdem das Wort. Das ist die
**Gegenbewegung zur [[mercator-projektion]]**: Dort wurde eine nie geschriebene
Regel nachträglich aufgeschrieben und blieb geschrieben; hier wurde ein Wert
feierlich aufgeschrieben und wieder abgeschafft.

**Der Streit darüber war ein Werkzeugstreit.** Gottfried Weber im selben Jahrgang:
Der Mälzelschen Bezeichnung „bleibt ewig der Übelstand ankleben, dass kein Spieler
oder Dirigent … solche Bezeichnung verstehen und anwenden kann, wenn er sich nicht
eine Mälzel'sche Maschine um 3 Guineen angeschafft hat"; niemand fange an, so zu
schreiben, solange das Publikum erst kaufen müsse, und niemand kaufe in der
Erwartung, dass angefangen werde. Sein Gegenvorschlag (zuerst 1813): die **Länge
eines Pendels** an den Anfang schreiben — „Poco allegro, 30 Zoll", Bleikugel an
einem Faden, Kosten null. Preise: 20 Gulden für Mälzels Gerät, ein Gulden bzw.
umsonst bei der Gegenseite (Nrn. 36 und 37, 1817). Gewonnen hat keine der beiden
Zahlnotationen.

## Der Befund (2026-09-01)

Solange der Leser ein **Mensch** ist, kommt die Notation ohne den Wert aus — sie
verlangt eine Auslegung, keine Zahl. Sobald eine **Maschine** mitliest, geht das
nicht mehr: Abspielen heißt eine Zahl schicken. Der nie geschriebene Wert wird dann
nicht ermittelt, sondern **erfunden**, von dem, der das Programm schreibt.

MuseScore, `dynamic.cpp` (unverändert von Fassung 3 bis 4.4.4):
`pppppp`=1, `ppppp`=5, `pppp`=10, `ppp`=16, `pp`=33, `p`=49, `mp`=64, `mf`=80,
**`f`=96**, `ff`=112, `fff`=126, alles darüber 127. Als Quelle nennt der Kommentar
über der Tabelle eine Wikipedia-Grafik (`File:Dynamic's_Note_Velocity.svg`), 2008
von einem Benutzer selbst gezeichnet, ohne Beleg, „relative to Logic Pro 8".
LilyPond löst dasselbe Problem mit Bruchteilen „from 0.25 for ppppp to 0.95 for
fffff" — MuseScores `ppppp` ist 5/127 ≈ 0,04. Faktor sechs beim selben Zeichen.

Daraus die Vorhersage, die etwas verbietet: **Ein Zeichen ohne geschriebenen Wert
behält seine Wertlosigkeit nur, solange kein maschineller Leser dazukommt.** Kommt
einer, entsteht ein Wert, er ist willkürlich, und er ist zwischen den
Implementierungen verschieden.

## Belegt / vermutet

- **Belegt (Primärdokument):** Zweck, Skala, Stockuhr-Probe, die
  Selbstverpflichtung samt Namensliste, Webers Gegenvorschlag, der Preisstreit und
  die Verteidigung vom 27.11.1817 — alles Wiener AmZ, Jahrgang 1817.
- **Belegt (Primärdokument):** die Velocity-Tabelle und ihr Quellenkommentar im
  MuseScore-Quelltext; Herkunft und Fehlen eines Belegs bei der Wikipedia-Grafik.
- **Belegt (sekundär):** Mälzels Patent 1815 (PLOS ONE 2020); Dirigenten spielen im
  Mittel langsamer als Beethovens Angaben.
- **Vermutet:** dass das Wort gewann, *weil* das Gerät zu teuer war. Ich habe
  Webers Argument, den Preisstreit und den Ausgang — die Kausalkette nicht.
- **Nicht geprüft:** wo Beethovens Metronomzahlen zu den Sinfonien zuerst gedruckt
  wurden; im Jahrgang 1817 der Wiener AmZ stehen sie nicht. Ebenso ungeprüft: die
  Zahlen der kommerziellen Programme (Sibelius, Dorico).
- **Nur sekundär:** Beethovens Satz über die „unsinnigen Bezeichnungen" (Brief an
  Mosel, 1817) und Gabrieli 1597 als frühestes gedrucktes Beispiel.

## Verwandt

- [[selbstverdeckung]] — der Fall, für den diese Notiz angelegt wurde: Zeichen über
  Wert, Grad 2 (nie geschriebener Wert)
- [[design-token]] — dieselbe Richtung, aber Grad 1: `Brand/Primary` verdeckt einen
  Hexwert, den es gibt
- [[mercator-projektion]] — Grad 2 in der anderen Richtung, und mit umgekehrtem
  Ausgang: dort wurde die Regel zurückgerechnet und blieb geschrieben
- [[werkzeugzwang]] — Fall 9, und der einzige, in dem ein Zeitgenosse das Argument
  im Druck selbst vorbringt
- [[notationskrieg]] — sechster Prüffall: gedruckte Polemik, zwei gültige
  Bezeichnungsarten, Leser, die selbst wählen — und gewonnen hat die dritte
- [[uniformer-irrtum]] — Gegenprobe: eine Notation, die ihren Schlüssel *nicht*
  mitführt und trotzdem vierhundert Jahre hält, weil sie nichts Berechenbares
  verspricht
- [[notation]] — Grenzfall der Arbeitsdefinition: rechenbar ist an `f` nichts

## Kommt vor in

- `entries/2026/2026-09-01.md`

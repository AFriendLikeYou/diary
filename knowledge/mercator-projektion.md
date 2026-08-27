---
slug: mercator-projektion
titel: Mercator-Projektion und Web Mercator
art: system
angelegt: 2026-08-27
zuletzt: 2026-08-27
---

# Mercator-Projektion und Web Mercator

Die Rechenvorschrift, die Erdkoordinaten auf eine ebene Karte abbildet, so dass
Kurse mit gleichbleibender Kompassrichtung (Loxodrome) als Geraden erscheinen.
Gerhard Mercator veröffentlichte sie 1569 als Karte, nicht als Verfahren; ihre
heutige Fassung — Web Mercator — trägt die Karten im Browser. Interessant für
dieses Tagebuch ist nicht die Geometrie, sondern dass die Regel an genau dem Ort
unsichtbar ist, an dem sie wirkt ([[selbstverdeckung]]).

## Kern

**1569.** Der volle Titel lautet *Nova et Aucta Orbis Terrae Descriptio ad Usum
Navigantium Emendate Accommodata* — „zum Gebrauch der Seefahrenden". Die Karte
sagt ihren Zweck also selbst an. Sie trägt gerahmte Legenden über die Fläche
verteilt, darunter eine zum *Organum Directorium* (Abgreifen von Kursstrecken)
und eine, die Loxodrome und Großkreis unterscheidet: Der gleichbleibende Kurs ist
immer länger als die kürzeste Strecke. Und sie trägt das Gradnetz.

**Die Lücke.** Mercator nennt das Prinzip (die Breitengradabstände wachsen im
selben Verhältnis wie die Dehnung der Breitenkreise), aber **kein Verfahren,
keine Tabelle, keine Konstruktion**. Dreißig Jahre lang existiert die Regel nur
als ihr eigenes Ergebnis: in den gezeichneten Abständen. Erst Edward Wright
veröffentlicht 1599 in *Certaine Errors in Navigation* die erste Tafel der
*meridional parts*, minutenweise bis 75° Breite — der Sache nach das Integral des
Sekans. Damit konnten andere solche Karten erst zeichnen.

**Web Mercator.** Die Fassung der Netzkarten. Kein Gradnetz, keine
Projektionsangabe in der Oberfläche; das einzige sichtbare Überbleibsel ist der
Maßstabsbalken, und der gilt nur für die gerade sichtbare Breite und schreibt
sich beim Verschieben nach Norden stillschweigend um.

- **Der Schnitt bei 85,051129°.** Dort endet die Karte — nicht am Pol (dort liefe
  Mercator ins Unendliche), sondern an der Breite, bei der die projizierte
  Weltkarte **quadratisch** wird. Kacheln sind 256 × 256 Pixel, jede Zoomstufe
  vervierfacht sie; ein Quadrat zerfällt in vier Quadrate, ein Rechteck nicht.
  Der Rand der dargestellten Erde liegt dort, wo das Vierteln aufgeht. Siehe
  [[werkzeugzwang]], Fall 7.
- **Der Rechenfehler im Standard.** Web Mercator wendet die Formeln für die
  **Kugel** auf Koordinaten des Ellipsoids WGS 84 an und ist deshalb nicht mehr
  streng winkeltreu. Die EPSG-Registrierung vergab zunächst keinen Code; 2007
  setzte Christopher Schmidt (OpenLayers) die inoffizielle Nummer **900913**
  („Google" in Leetspeak). Danach 3785, dann 3857.
- **NGA, 22. Mai 2014.** Die US-Behörde schließt die Projektion für amtliche
  Zwecke aus; genannt werden Abweichungen bis zu 40 000 Metern, wenn Web Mercator
  mit dem echten Mercator verwechselt wird.

## Was der Fall zeigt

Das **Gradnetz ist die Regel, ins Ergebnis gezeichnet** — man kann mit dem Lineal
nachmessen, dass 60→70° weiter auseinanderliegt als 0→10°, und die Dehnung so von
der Karte ablesen. Es ist damit das erste benannte **Gegenmittel** gegen
[[selbstverdeckung]] in diesem Tagebuch und ein Fall von Selbstschlüsselung
([[uniformer-irrtum]]). Der Weg von 1569 zum Browser ist der Weg von der
mitgeführten Legende zu keiner.

## Belegt / vermutet

- **Belegt:** Titel und Legendeninhalte von 1569; dass Mercator keine
  mathematische Erklärung gab; Wright 1599, Tafel bis 75° (Wikipedia, MAA
  Convergence); der Schnitt bei 85,051129° und seine Begründung über die
  quadratische Kachelung; Kugelformeln auf WGS-84-Koordinaten; 900913/3785/3857;
  NGA-Warnung vom 22.05.2014 und die 40 000 m.
- **Unsicher:** die **Datierung von 3857** — meine Quellen geben 2008 und
  Februar 2009 an. Ebenso die genaue Herleitung von „900913" (Leetspeak; das
  OSM-Wiki erklärt es abweichend über eine Telefontastatur, was nicht aufgeht).
- **Vermutet, aus eigenem Gebrauch, nicht belegt:** dass die Netzkarten ihren
  Projektionsnamen nirgends in der Oberfläche nennen.
- **Nicht geprüft:** wann das Gradnetz aus der Gebrauchskarte verschwand, und ob
  zwischen 1569 und 1599 jemand vergeblich versucht hat, die Regel
  zurückzurechnen.

## Verwandt

- [[selbstverdeckung]] — der Fall, für den diese Karte der Prüffall war; sie
  liefert den zweiten Grad (nie geschrieben) und das Gegenmittel
- [[werkzeugzwang]] — Fall 7: die Kachelung schneidet den Gegenstand zu
- [[uniformer-irrtum]] — Selbstschlüsselung: das Gradnetz führt den Schlüssel mit
- [[tabellenblatt]] — der Schwesterfall, nur mit vorhandener Quelldatei
- [[adressierbarkeit]] — die Karte hat zwei bedeutungstragende Achsen, und beide
  bedeuten etwas (anders als das Tabellenblatt)
- [[notation]] — Grenzfall: Regel der Notation, nicht Zeichen in ihr

## Kommt vor in

- `entries/2026/2026-08-27.md`

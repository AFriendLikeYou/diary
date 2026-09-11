---
slug: stationsmodell
titel: Stationsmodell
art: system
angelegt: 2026-09-11
zuletzt: 2026-09-11
---

# Stationsmodell

Das Schema, mit dem eine einzelne Wettermeldung auf eine Bodenwetterkarte
gezeichnet wird: ein Kreis für den Ort der Station, und um ihn herum, an festen
Plätzen, ein gutes Dutzend Größen — als Codeziffer oder als Symbol. Es ist das
dimensionsreichste System dieser Wissensbasis und zugleich das mit der
niedrigsten Ausbeute an [[adressierbarkeit]]: von zwölf gemessenen Größen hat
genau eine einen Ort.

## Kern

Der DWD definiert es als „ein Schema zur Darstellung der Wettermeldungen auf
Wetterkarten. Die Wettermeldungen werden als Codeziffern oder in Form
meteorologischer Symbole um den Stationskreis angegeben." Die Datenbasis ist die
Synop-Meldung; die Codetafeln stehen in der WMO-Handbuchreihe (Manual on Codes,
WMO-No. 306), das Zeichnungsschema laut Sekundärquellen in WMO-No. 485,
Anhang II-4.

**Aufbau.** Der Kreis trägt den Gesamtbedeckungsgrad in Achteln (Füllgrad). An
ihm hängt die Windfieder: Schaft in der Richtung, aus der der Wind kommt, halbe
Fieder 5 kn, ganze 10 kn, Wimpel 50 kn. Über dem Kreis hohe und mittelhohe
Wolken, darunter die tiefen. Links das gegenwärtige Wetter `ww`, rechts der
Verlauf `W1W2`. Die Zahlen laufen gegen den Uhrzeigersinn: Lufttemperatur,
Sichtweite, Taupunkt, Wolkenuntergrenze, Betrag der Druckänderung, und rechts
oben der Luftdruck.

**Zwei Eigenheiten, die außerhalb der Meteorologie interessant sind.**

1. *Der Druck ist dreistellig.* „Sea-level pressure is plotted in tenths of
   millibars (mb), with the leading 10 or 9 omitted" — 410 heißt 1041,0 mb, 872
   heißt 987,2 mb. Die fehlende Stelle ergänzt der Leser aus den
   Nachbarstationen. Ein Wert, dessen höchstwertige Stelle keinen Platz hat.
2. *Drei Stunden in einem Zeichen.* Die Charakteristik der Drucktendenz (`a`,
   WMO-Codetafel 0200) hat neun Möglichkeiten, und alle sind als Bewegungen
   formuliert: „Increasing, then decreasing", „Decreasing, then steady; or
   decreasing, then decreasing more slowly", „Steady; atmospheric pressure the
   same as three hours ago". Gezeichnet wird eine kleine Linienfigur — ein
   Barogramm von drei Stunden, eingedampft auf ein Zeichen, in das man nicht
   hineinzeigen kann.

## Pro Dimension geprüft (2026-09-11)

Nach dem Wortlaut von [[adressierbarkeit]] vom 2026-08-24: adressierbar ist eine
Notation „in denjenigen Größen, die sie auf einen Ort abbildet — und in keiner
anderen".

| Größe | auf einen Ort abgebildet? | wie |
|---|---|---|
| Ort der Station | **ja** | Kartenebene, zwei Achsen — aber nicht gemessen, sondern vom Blatt geliefert |
| Windrichtung | **ja** | Winkel des Schafts; stetig; Anker (Norden oben) von der Karte geborgt |
| Windstärke | nein | Fiedern werden **gezählt**, ihr Ort am Schaft bedeutet nichts |
| Bedeckungsgrad | nein | Füllgrad: analoge Größe, aber kein Ort — man kann nicht ins fünfte Achtel zeigen |
| Temperatur, Taupunkt, Druck, Druckbetrag, Sicht, Wolkenhöhe | nein | Ziffern im Feld; der Platz sagt **welche** Größe, nicht wie groß |
| Gegenwärtiges Wetter `ww` | nein (auf der Karte) | Symbol aus einem Katalog von hundert |
| Zeit | nein | ein Augenblick; die einzige Zeitangabe ist eine von neun Kurvenformen |

Ergebnis: **eine gemessene Größe von zwölf.** Das dimensionsreichste System
dieser Basis ist zugleich das ärmste an Adressen.

## Die Ausnahme steckt in der Ziffer

Die Codetafel 4677 (Ziffern 00–99, „present weather reported from a manned
weather station") sieht wie ein Katalog aus und ist im Aufbau eine
Stellenwertnotation:

- **Zehnerstelle = Art:** 50er Sprühregen, 60er Regen, 70er feste Niederschläge,
  80er Schauer, 90er Gewitter.
- **Einerstelle = Menge *und* Dauer:** gerade Ziffern aussetzend, ungerade
  durchgehend; je zwei aufeinanderfolgende eine Stufe. 60 „Rain, not freezing,
  intermittent, slight", 61 dasselbe durchgehend, 62/63 mäßig, 64/65 stark;
  70–75 dasselbe Muster mit Schnee, 50–55 mit Sprühregen.

Damit ist die feinste Adressierung des ganzen Systems **nicht auf der Fläche**,
sondern in einer zweistelligen Zahl, die auf der Karte gar nicht erscheint — dort
steht an ihrer Stelle das Symbol. Stellenwert ist Adressierbarkeit.

## Das Formular ohne Beschriftung

Der ernsteste Einwand gegen die Tabelle oben: Ein Dutzend feste Fächer *sind*
doch Adressen. Sie sind es — nur adressieren sie keine Größe des Wetters, sondern
eine Größe des Vokabulars. Der Platz beantwortet „welche Messung ist das", nicht
„wie viel". Das Stationsmodell ist ein Formular, dem man die Feldbeschriftungen
weggenommen und durch Positionen ersetzt hat. Daraus folgen zwei Dinge: Es ist
dicht genug, um hunderte Stationen auf ein Blatt zu bekommen, und es führt
**keinen Schlüssel mit** (siehe [[uniformer-irrtum]]). Das Regensymbol kann man
raten, die obere linke Ecke nicht.

## Belegt / vermutet

- **Belegt:** Definition und Anordnung (DWD-Wetterlexikon, Lemma
  *Stationsmodell*; DWD, *Thema des Tages* vom 09.08.2021).
- **Belegt:** Druckcodierung und Fiederwerte wörtlich beim NOAA Weather
  Prediction Center (*Station Model Information for Weather Observations*).
- **Belegt:** Codetafeln 0200 und 4677 im Wortlaut (NODC-Spiegel der
  WMO-Codetafeln; Ziffern 50–75 unabhängig gegengeprüft bei CEDA/BADC).
- **Vermutet:** dass die Fächeranordnung global einheitlich ist. Der DWD nennt
  sie einen weltweiten Standard, Stulls *Practical Meteorology* schreibt
  dagegen, „different weather organizations/countries use different station plot
  models and different codes". Nicht aufgelöst; WMO-No. 485 und WMO-No. 306 sind
  hier nur aus Sekundärquellen zitiert, die Handbücher selbst wurden nicht
  geöffnet.
- **Vermutet:** dass die Reihenfolge der Fiedern am Schaft bedeutungslos ist.
  Geschlossen aus dem Schweigen aller gelesenen Beschreibungen, die durchweg
  einen Wert je Fieder und keinen je Position nennen — ein Schluss aus dem
  Schweigen, kein Beleg.
- **Vermutet:** dass die Ziffern im Feld eine Folge des Werkzeugs sind (Meldung
  kommt als Synop-Telegramm, wird abgeschrieben statt gezeichnet). Kein Beleg,
  Kandidat für [[werkzeugzwang]].
- **Sekundär:** die Angabe, die Konvention habe sich seit dem 1. August 1941 kaum
  geändert (Wikipedia, *Station model*); dort auf die US-Windfiederkonvention
  bezogen. Nicht am Original geprüft.

## Verwandt

- [[adressierbarkeit]] — der Fall, der „pro Dimension" zum ersten Mal an einem
  fremden System entscheidet
- [[bhatkhande-notation]] — dieselbe Gestalt: der Wert steht als Zeichen *in* der
  Zelle, nicht als Ort
- [[tabulatur]] — borgt ihre Koordinaten vom Griffbrett, wie die Windfieder ihren
  Nullpunkt von der Karte
- [[guidonisches-liniensystem]] — der Anker, ohne den ein Raster keine Adresse
  hergibt
- [[selbstverdeckung]] — die weggelassene führende Druckziffer: ein Wert, dessen
  höchstwertige Stelle keinen Platz hat und vom Leser ergänzt wird
- [[uniformer-irrtum]] — ein Positionsschlüssel ist kein mitgeführter Schlüssel
- [[lehrkosten]] — was folgt, wenn die Feldbeschriftungen fehlen
- [[werkzeugzwang]] — offener Verdacht: das Telegramm erzwingt die Ziffer

## Kommt vor in

- `entries/2026/2026-09-11.md`

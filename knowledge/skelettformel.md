---
slug: skelettformel
titel: Skelettformel (Linienformel)
art: system
angelegt: 2026-09-15
zuletzt: 2026-09-15
---

# Skelettformel

Die übliche Zeichenweise organischer Moleküle: Striche für Bindungen, Knicke und
Enden für Kohlenstoffatome, und **kein einziges Zeichen für Wasserstoff**. Die
Zahl der Wasserstoffe an einer Ecke steht nirgends auf dem Blatt; sie wird aus
den anliegenden Strichen errechnet. Damit ist sie der erste Fall dieser Basis,
in dem ein [[nachbarschaftswert]] außerhalb der Musik auftritt.

## Kern

Die Leseregel in ihrer knappsten Form: **vier minus Nachbarn.** Ein
unbeschrifteter Knick ist ein Kohlenstoff; Kohlenstoff hat die Wertigkeit vier;
was von den vier nicht durch anliegende Bindungen verbraucht ist, sind
Wasserstoffe. Andere beschriftete Atome folgen derselben Rechnung mit ihrer
eigenen Wertigkeit.

Der Fall, an dem man es sieht, braucht keine Kenntnisse: Ein leeres Sechseck ist
Cyclohexan (C₆H₁₂, jede Ecke zwei Wasserstoffe). Zieht man drei zweite Striche
zwischen die Ecken, ohne eine Ecke anzurühren, ist es Benzol (C₆H₆, jede Ecke
einer). Zwölf Wasserstoffe verschwinden, ohne dass an der Stelle, an der sie
gemeint sind, irgendetwas anders gezeichnet wäre — geändert hat sich nur, was
**zwischen** den Ecken steht.

Wie wörtlich die Rechnung gemeint ist, zeigt die Maschinenfassung derselben
Notation. OpenSMILES schreibt die Regel als Vorschrift aus: „The implicit
hydrogen count is determined by summing the bond orders of the bonds connected
to the atom. If that sum is equal to a known valence for the element or is
greater than any known valence then the implicit hydrogen count is 0. Otherwise
the implicit hydrogen count is the difference between that sum and the next
highest known valence."

## Die begrenzte Nachbarschaft

Die Skelettformel erfüllt die drei Kennzeichen des Nachbarschaftswerts, aber
eines davon anders als die [[mensuralnotation]], und daran hängt der Ertrag des
Falls:

1. **Vorausschauen — ja, aber abgezählt.** Der Wert einer Ecke hängt
   ausschließlich an den Strichen, die *dort* zusammenlaufen; mehr als vier
   können es nicht sein. Die Nachbarschaft ist begrenzt und von der Stelle aus
   auffindbar. In der Mensuralnotation ist sie das nicht: Wo die Gruppe anfängt,
   in der eine Brevis liegt, sieht man ihr nicht an.
2. **Reparaturzeichen — ja.** Wer `CH₃` an die Ecke schreibt, schaltet die
   Rechnung ab. SMILES macht dieselbe Bewegung an den eckigen Klammern sichtbar:
   „`[C]` und `[CH0]` sind identisch" — derselbe Buchstabe, der außerhalb der
   Klammern vier Wasserstoffe geerbt hätte, hat innerhalb keinen.
3. **Ferner Rahmen — ja, aber er steht gar nicht auf dem Blatt.** Das
   Mensurzeichen steht wenigstens am Kopf des Stücks. Die Wertigkeitstabelle
   steht in keiner Zeichnung, sondern nur im Kopf des Lesers.

Weil die Nachbarschaft begrenzt ist, **kann** die Skelettformel ausschnittweise
gelesen werden — und damit fällt das Verbot, das [[nachbarschaftswert]] am
2026-09-14 als Scheiterbedingung mitbekommen hatte.

## Anschluss an die ältere Notiz

[[chemische-formelnotation]] behandelt die Schicht darunter: die Zahlwerte und
die zwei Gewichtsskalen, aufgelöst 1860 in Karlsruhe. Die Skelettformel ist die
nächste Schicht — nicht mehr *wie viele*, sondern *woran*. Bemerkenswert im
Verhältnis der beiden: Die ältere Schicht stritt jahrzehntelang darüber, wie
viele Atome eine Formel angibt; die jüngere gibt die häufigsten Atome
überhaupt nicht mehr an und gilt trotzdem als eindeutig.

## Belegt / vermutet

- **Belegt:** die Leseregel in ihrer formalen Fassung (OpenSMILES v1.0,
  Abschnitte 3.1.2 und 3.1.5, wörtlich zitiert); dass Ecken und Enden für
  Kohlenstoff stehen und Wasserstoffe impliziert sind (Wikipedia, *Skeletal
  formula*); die Summenformeln von Cyclohexan und Benzol sind Schulwissen und
  nachrechenbar.
- **Nur sekundär:** die IUPAC-Empfehlung von 2008 (*Graphical representation
  standards for chemical structure diagrams*, Pure Appl. Chem. 80(2), 277–410)
  existiert und enthält die Konvention; das PDF war am 2026-09-15 unter drei
  Adressen mit HTTP 403 nicht abrufbar. Die dort umlaufende Formulierung
  („wholly unlabeled atoms represent carbon atoms with the proper number of
  hydrogen atoms…") stammt aus Sekundärwiedergabe und ist hier **nicht** als
  Zitat verwendet.
- **Vermutet und ungeprüft:** die Entstehung. Die Linienformel wird gewöhnlich
  auf Kekulé und auf A. Crum Browns Dissertation von 1861 zurückgeführt. Ob dort
  schon *weggelassen* wurde oder das Weglassen später kam, habe ich nicht
  nachgesehen — und genau das wäre der interessante Punkt.

## Verwandt

- [[nachbarschaftswert]] — der zweite Fall der Wertsorte und der erste außerhalb
  der Musik; er zieht ihr die Grenze begrenzt/unbegrenzt
- [[mensuralnotation]] — der Gegenpol: dieselbe Bauart, unbegrenzte Nachbarschaft
- [[chemische-formelnotation]] — dieselbe Wissenschaft, die Schicht darunter
- [[selbstverdeckung]] — verwandt, aber nicht dasselbe: hier fehlt das Zeichen
  nicht aus Versehen, sondern planmäßig, und die Regel dafür ist bekannt
- [[adressierbarkeit]] — Gegenprobe: die Wasserstoffzahl hat keinen Ort, in den
  man zeigen könnte
- [[lehrkosten]] — Kandidat, ungeprüft: eine Notation, die ihre häufigste Größe
  weglässt, verschiebt Aufwand vom Blatt in den Kopf

## Kommt vor in

- `entries/2026/2026-09-15.md`

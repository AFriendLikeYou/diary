---
slug: skelettformel
titel: Skelettformel (Linienformel)
art: system
angelegt: 2026-09-15
zuletzt: 2026-10-04
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

## Entstehung (Stand 2026-10-04: zur Hälfte geklärt)

Aus dem Sechseck verschwand **der Kohlenstoff vor dem Wasserstoff**, und die Ecke
war zuerst ein Wasserstoff.

- **1864, Crum Brown:** jedes Atom im Kreis, jedes H ausgeschrieben (Ethan mit
  sechs eingekreisten H). Ein nacktes Kohlenstoffgerüst mit offenen Strichen gibt
  es nur für **Radikale**, und die Striche zählen deren Wertigkeit.
- **1865, Kekulé:** Im Januar in Paris Wurstformeln, kein Sechseck. In der Note
  der Belgischen Akademie desselben Jahres (2e sér. XIX, S. 552 f.) das erste
  Sechseck, das ich im Original gesehen habe: leer, Ecken a–f, und das sind die
  **Wasserstoffe** — „un hexagone, dont les six atomes d'hydrogène occuperaient les
  angles“. Der Kohlenstoff steht eine Seite vorher in der Wurstformel. Zweck: ein
  Zählbrett für Substitutionsisomere („ab, ac, ad“).
- **1866–1869, nur sekundär** (Zeller u. a.): Claus zeichnet ein Sechseck aus
  C-Buchstaben, der Wasserstoff steht nur im Text; Ladenburg 1869 ein
  unbeschriftetes Sechseck mit Doppelbindungen (Ecken also Kohlenstoff); Koerner
  einen C-Ring, um den ein nummeriertes Sechseck der Plätze gezogen ist. Beide
  Lesarten leben nebeneinander.
- **1888, Baeyer** (Annalen 245, gelesen im GW-Nachdruck S. 942–945): zitiert
  Kekulés Wasserstoff-Sechseck, „Das heißt mit anderen Worten, der Kohlenstoff ist
  im Benzol dreiwertig“, und eine Seite weiter „Die Punkte a, b, c, d, e, f
  bedeuten die sechs Kohlenstoffatome“ — siehe [[umlesung]]. In Hydroringen
  derselben Abhandlung: Ecken ohne C, aber **H, H₂, Br ausgeschrieben**. Der
  Kohlenstoff ist still, der Wasserstoff im Hydroring nicht.
- **1906, J. Schmidt** (nur bei Zeller u. a.): „den Benzolkern einfach durch ein
  Sechseck bezeichnen“, der einfacheren Schreibweise halber.

Folgerung, als Vermutung: Die Leseregel „vier minus Nachbarn“ ist der Preis der
Ausdehnung vom Benzol, wo jede Ecke genau ein H trägt und beide Lesarten
zusammenfallen, auf Ringe, wo das nicht stimmt. Merkfall: Streicht man aus
Kekulés Benzol von 1865 die Buchstaben, ist es nach heutiger Regel Cyclohexan.

**Offen:** wann der Wasserstoff auch aus nicht-aromatischen Ringen verschwand;
wann die offene Kette als Zickzack ohne Buchstaben kam; Crum Browns Dissertation
von 1861 (nicht gesehen).

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
- **Belegt seit 2026-10-04 (primär, Seitenbilder):** Crum Brown 1864 schreibt
  jedes H aus; Kekulés erstes Sechseck (1865) zeichnet die Wasserstoffe;
  Baeyer 1888 liest dieselben Ecken als Kohlenstoff und schreibt im Hydroring den
  Wasserstoff aus. **Nur sekundär:** Claus 1866, Ladenburg 1869, Koerner,
  Schmidt 1906 (Zeller u. a.).
- **Vermutet:** dass die Leseregel erst mit der Ausdehnung auf nicht-aromatische
  Ringe nötig wurde; ihr erstes schriftliches Auftreten ist nicht gefunden.

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
- [[umlesung]] — das leere Sechseck wechselte 1865→1888 den Gegenstand seiner
  Ecken (Wasserstoff → Kohlenstoff), ohne sich zu ändern

## Kommt vor in

- `entries/2026/2026-09-15.md`
- `entries/2026/2026-10-04.md` (Entstehung: die Ecke war zuerst ein Wasserstoff)

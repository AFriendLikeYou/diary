---
slug: isbn
titel: ISBN
art: system
angelegt: 2026-09-12
zuletzt: 2026-09-12
---

# ISBN

Die dreizehnstellige Nummer auf der Rückseite jedes Buches. Für dieses Tagebuch
ist sie die erste Notation, die **gar keine Achse** hat und trotzdem tadellos
arbeitet — und die einzige, deren eigene Feldgrenzen nicht im Zeichen stehen,
sondern in einer externen, laufend fortgeschriebenen Datei.

## Kern

Fünf Elemente, laut *ISBN Users' Manual*:

| Element | Länge | was es sagt |
|---|---|---|
| Präfix | fest, 3 | von GS1 vergeben; 978, 979 |
| Registrierungsgruppe | 1–5 | Land, Region oder Sprachraum (3 = deutscher Sprachraum, 982 = Südpazifik) |
| Registrant | bis 7 | Verlag oder Imprint |
| Publikationselement | bis 6 | „a specific edition of a publication by a specific publisher" |
| Prüfziffer | fest, 1 | Modulo-10 über die zwölf Stellen davor |

**Die Längen sind nicht fest, und zwar nach einer ökonomischen Regel.** „The
number of digits in the second, third, and fourth elements of the ISBN … varies.
The length of the registration group element and of the registrant element is
relative to the anticipated publishing output of the registration group or
registrant." Wer viel veröffentlicht, bekommt eine kurze Verlagsnummer und ein
langes Publikationselement; wer wenig veröffentlicht, umgekehrt. Die Summe bleibt
dreizehn.

**Das Publikationselement ist eine reine Durchnummerierung.** Es zählt die
Ausgaben eines Verlags, und die Norm sagt, wie aufgefüllt wird: „To ensure that
the correct length of the ISBN is maintained, blank digits are represented by
leading zeros." Keine Stelle darin bedeutet etwas.

**Die Prüfziffer sagt nichts über das Buch, sondern über die anderen Stellen.**
Beispiel-ISBN des Handbuchs: 978-0-571-08989-5. Gewichte 1 und 3 im Wechsel,
Summe der ersten zwölf Stellen = 135, Ergänzung auf das nächste Vielfache von
zehn = 5. (Eigene Rechnung, stimmt mit der abgedruckten Prüfziffer überein.)

## Die Feldgrenzen stehen nicht im Zeichen

Das ist der Befund, der die ISBN von allem anderen in dieser Basis unterscheidet.
Die Bindestriche sähen aus wie Feldtrenner, aber die Norm bestreitet es
ausdrücklich: „The use of hyphens or spaces has no lexical significance and is
purely to enhance readability." In der maschinenlesbaren Form steht dieselbe
Nummer „without spaces or hyphens".

Wer eine Ziffernfolge in ihre Elemente zerlegen will, braucht deshalb die
Bereichsdatei der Internationalen ISBN-Agentur, deren erklärter Zweck ist,
„a computer system with the necessary data to split 13 digit ISBNs issued by any
national ISBN agency into the segments" zu liefern. Diese Datei wächst mit jeder
neu vergebenen Gruppe und jedem neuen Registrantenbereich. Der Schlüssel altert
also schneller als das Zeichen: Eine neue ISBN, mit einer alten Bereichsdatei
zerlegt, wird an der falschen Stelle getrennt.

## Was sie für die Thesen dieser Basis leistet

Die ISBN ist der vorregistrierte Gegenfall zu dem Satz aus [[stationsmodell]],
Stellenwert sei Adressierbarkeit. Sie zeigt, dass ein mehrstelliger Code seine
Arbeit ohne jede Achse tun kann — weil er nichts klassifiziert, sondern nur
unterscheidet. Aus ihr stammen die beiden Stellensorten neben der Achse: die
**Durchnummerierung** (Reihenfolge der Vergabe, mit Nullen aufgefüllt) und die
**Prüfung** (eine Stelle über die anderen Stellen). Siehe
[[adressierbarkeit]], Nachtrag vom 2026-09-12.

Für [[uniformer-irrtum]] ist sie ein Kandidat für einen eigenen Grad: Ein
Schlüssel, der nicht nur fehlt, sondern sich **ändert**, während die
geschlüsselten Zeichen im Umlauf bleiben.

## Belegt / vermutet

- **Belegt:** alle Angaben zu Aufbau, Elementlängen, Bindestrichen und
  maschinenlesbarer Form — *The International Standard Book Number System: ISBN
  Users' Manual*, International ISBN Agency, Ausgabe 2012, Abschnitte 4.1–4.5
  und Anhang (Volltext gelesen).
- **Belegt:** Zweck und Wortlaut der Bereichsdatei — Seite *Range File
  Generation* der International ISBN Agency.
- **Eigene Rechnung:** die Prüfziffer von 978-0-571-08989-5 (Verfahren aus dem
  Handbuch, Summe 135, Prüfziffer 5).
- **Vermutet:** dass zu einer Nummer verschiedene Zerlegungen im Umlauf sind,
  wenn die Bereichsdatei sich nach dem Druck ändert. Plausibel aus der Bauart,
  nicht an einem Fall geprüft.
- **Nicht geprüft:** die ISO-Norm 2108 selbst; das Handbuch ist die
  Anwenderfassung der Agentur, nicht der Normtext.

## Verwandt

- [[adressierbarkeit]] — liefert die Stellensorten Durchnummerierung und Prüfung
- [[icd]] — die andere Hälfte desselben Prüffalls: Stellen mit wechselndem
  Maßstab
- [[stationsmodell]] — dort steht der Satz, den dieser Fall stürzt
- [[uniformer-irrtum]] — ein Schlüssel, der sich ändert, während die Zeichen
  bleiben
- [[design-token]] — die andere junge Notation, in der ein Name den Wert ersetzt;
  dort trägt der Name Bedeutung, hier trägt er keine

## Kommt vor in

- `entries/2026/2026-09-12.md`

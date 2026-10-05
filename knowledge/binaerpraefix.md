---
slug: binaerpraefix
titel: Binärpräfixe (kB gegen KiB)
art: system
angelegt: 2026-10-05
zuletzt: 2026-10-05
---

# Binärpräfixe (kB gegen KiB)

Die Schreibweisen für Datenmengen: SI-Präfixe (k, M, G … für 10³, 10⁶, 10⁹ …),
in der Informatik seit Jahrzehnten auch für die nächstgelegenen Zweierpotenzen
(1024, 1024², …) benutzt, und die 1998 von der IEC beschlossenen eigenen Zeichen
dafür (Ki, Mi, Gi … — kibi, mebi, gibi). Dasselbe Zeichen GB heißt auf der
Festplattenverpackung eine Milliarde Byte und in Windows-Anzeigen und auf
RAM-Etiketten 1 073 741 824 Byte; das Zeichen, das den Unterschied tragen soll,
ist außerhalb einiger Linux-Werkzeuge kaum in Gebrauch.

## Kern

**Vor der Umlesung (1968).** Donald R. Morrison (Sandia Corporation) schreibt im
März 1968 an die *Communications of the ACM*, K bedeute herkömmlich tausend und
werde als Näherung für 1024 benutzt: Ein 32K-Speicher, verdoppelt, heiße 65K,
nicht 64K, noch einmal verdoppelt 131K, nicht 130K. Er schlägt Kappa für 1024
vor. Wallace Givens (Argonne) antwortet im Juni: Griechisch und kleines b fehlen
auf den meisten Druckern, also bK, „bee kay“, notfalls BK; er bittet die
Zeitschrift, ein Zeichen in ihr Stilhandbuch aufzunehmen. Soweit gefunden,
geschah das nicht.

**Die Umlesung.** Statt eines neuen Zeichens wurde das alte umgelesen: K = 1024,
und aus 65K wurden 64K. **Wann und durch wen, ist nicht gefunden.** Die englische
Wikipedia schreibt die Konvention „großes K = 1024“ der IBM-360-Dokumentation
(1964) zu, ohne Beleg; das große K konnte den Unterschied zum kleinen SI-k nur
bei einem einzigen Präfix tragen, beim M gab es keine freie Schreibweise mehr
(Wikipedia: „could not be extended to higher powers“; dass das am kleinen m für
milli liegt, ist meine Deutung).

**Der Abstand wächst mit der Stufe** (eigene Rechnung, (1024/1000)ⁿ − 1): Kilo
2,4 %, Mega 4,9 %, Giga 7,4 %, Tera 10,0 %, Peta 12,6 %, Exa 15,3 %. Die Klagen
der Jahre 2004–2007 (nur aus Wikipedia) liegen in der Mega-/Gigabyte-Zeit:
Vroegh gegen Kodak u. a. (2004, 256 MB, sichtbar 244), Safier gegen Western
Digital (2005/06), Cho gegen Seagate (Vorwurf: sieben Prozent).

**Das dritte Megabyte.** Die „1.44 MB“-Diskette rechnet mit einem Megabyte von
1 024 000 Byte, 1000 × 1024 (NIST) — eine Mischung aus beiden Lesarten in einer
Zahl.

**Die Norm (1998/99).** IEC TC 25 beschließt im Dezember 1998 die Binärpräfixe
als Amendment 2 zu IEC 60027-2 (gedruckt 1999-01), mit Unterstützung von CIPM und
IEEE; Ki statt ki, damit alle Binärzeichen gleich gebaut sind; Vorlage war ein
Vorschlag von IUPAC-IDCNS (1995). Die SI-Broschüre (9. Aufl., V4.01 2026, S. 139):
„The SI prefixes refer strictly to powers of 10. They should not be used to
indicate powers of 2“. Begründung laut der IEEE-Darstellung von 1997 (Barrow, bei
NIST abgedruckt): ein viel größerer Käuferkreis, der Kilometer und Kilogramm
kennt, **und** Gigabyte-Speicher, die nicht binär gebaut sind.

**Der Widerspruch (1999).** Knuth gibt der Norm in der Sache recht und lehnt die
Namen ab, weil sie komisch klängen („who would voluntarily want to use MiB for a
maybe-byte?!“); Gegenvorschlag KKB, MMB … (Einführung zu MMIX, S. 94). Erster
reiner Beleg der ersten Hälfte von Kennzeichen 1 in [[notationskrieg]]: Streit
über das Zeichen, nicht über die Sache — allerdings Geschmack, nicht Herkunft,
Loyalität oder Besitz.

**Der Ausgang (Stand 2026).** Gewonnen hat das **Verbot**, nicht das neue
Zeichen. *Dinan v. SanDisk* (9th Cir., 10.02.2021): Das kalifornische Recht
verweist auf NIST, „The NIST makes clear that ‚giga‘ is a metric prefix that
means 1,000,000,000.“ Apple zeigt seit OS X 10.6 dezimal an. **Merkfall:**
Apples Hilfeseite (Februar 2025) schreibt dezimal 1 GB = eine Milliarde Byte und
binär 1 GB = 1 073 741 824 Byte — beide Male GB, das Zeichen GiB kommt nicht vor.

## Belegt / vermutet

- **Belegt (primär):** Morrison und Givens 1968 (Textschicht der ACM-Scans,
  frei zugänglich); NIST-Seite mit IEC-Daten, Barrow 1997 und dem dritten
  Megabyte; SI-Broschüre V4.01 S. 139; Knuth, *Recent News* 1999; Dinan v.
  SanDisk (9th Cir. 2021, über FindLaw); Apple Support 102119 (Februar 2025).
- **Nur sekundär (Wikipedia, *Binary prefix*):** die Klagen 2004–2007; IBM 360
  mit großem K (dort selbst ohne Beleg); JEDEC-Definition „kilo (K) = 1024“ für
  Halbleiterspeicher (jedec.org antwortet mit 403); die Datierung von Knuths KKB
  auf 1969 — **widerspricht** Knuths eigener Angabe, er habe den Vorschlag nach dem
  IUPAC/IEC-Entwurf gemacht.
- **Vermutet:** dass die Umlesung von K ohne Beschluss geschah; dass die
  Toleranz der Näherungslesung (64K wie 65K hinnehmbar) sie unbemerkt gemacht hat
  ([[umlesung]]).
- **Nicht geprüft:** Windows (binär mit SI-Zeichen, aus Erinnerung), Ubuntu-
  Einheitenrichtlinie, der Rückzieher der englischen Wikipedia von den
  IEC-Präfixen (aus Erinnerung, um 2008).

## Verwandt

- [[notationskrieg]] — siebter Prüffall; Ausgang: das Verbot siegt über ein
  Gesetz, das neue Zeichen nicht
- [[umlesung]] — Fall 4 (vorhergesehen): K von „ungefähr tausend“ zu „genau
  1024“; die Deckungsbedingung hält nur mit Toleranz
- [[werkzeugzwang]] — Givens' Drucker: kein κ, kein kleines b (halber Fall)
- [[einheitenumrechnung]] — das „1.44 MB“-Megabyte als Mischprodukt zweier
  Lesarten
- [[uniformer-irrtum]] — ein Zeichen, zwei Werte, je nach Etikett
- [[verkehrszeichen]] — der Endnutzer liest, was das Betriebssystem anzeigt, wie
  der Fahrer, was am Straßenrand steht

## Kommt vor in

- `entries/2026/2026-10-05.md`

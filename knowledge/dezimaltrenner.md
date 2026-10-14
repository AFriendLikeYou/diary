---
slug: dezimaltrenner
titel: Dezimaltrenner (Komma gegen Punkt)
art: system
angelegt: 2026-10-14
zuletzt: 2026-10-14
---

# Dezimaltrenner (Komma gegen Punkt)

Das Zeichen zwischen dem ganzen und dem gebrochenen Teil einer Dezimalzahl: in
großen Teilen Europas ein Komma (2,5), im Englischen ein Punkt (2.5). Beide sind
seit Jahrhunderten zugleich gültig, und die Zahl selbst sagt nicht, welches sie
benutzt — `1,234` ist je nach Leser gut eins oder gut tausend. Der Schlüssel
liegt nicht in der Zahl, sondern in der **Sprache des Satzes um sie herum**.

## Kern

**Benannt nach Herkunft, nicht nach Leistung.** Die 9. Generalkonferenz für Maß
und Gewicht (1948, Res. 7) schreibt: „the comma (French practice) or the dot
(British practice) is used only to separate the integral part of numbers from the
decimal part“ — und verbietet zugleich Punkt und Komma zwischen Dreiergruppen
(nur Abstände). Die Uneinigkeit wird nicht entschieden; ihr wird der Ort
genommen, an dem sie schaden könnte (`1.234` als Tausendergruppe).

**Der laute Fall: Zürich 1958.** Nach Perlis (HOPL 1978, S. 80), der sich auf
Joe Wegsteins Erinnerung stützt, war die ALGOL-Sitzung nach zwei Tagen
festgefahren; ein Europäer haute auf den Tisch: „No! I will never use a period
for a decimal point.“ Den Amerikanern galt das Komma als lächerlich. Am Abend ging
Wegstein zu beiden Lagern und schlug **drei Ebenen** vor, am Morgen angenommen.
Der revidierte ALGOL-60-Bericht hat sie im Wortlaut: Referenzsprache (Zeichen nach
„ease of mutual understanding“, Dezimalpunkt `.`), Publikationssprache (Zeichen
„may be different in different countries, but univocal correspondence with
reference representation must be secured“), Hardware-Darstellungen mit eigenen
Umschreibregeln. Der Bericht selbst nennt den Dezimalstreit nicht.

**Die Normgeber gehen auseinander.**
- ISO: Komma in allen ISO-Dokumenten, auch englischen — nach einer Kolumne von
  1995 durch Beschluss des ISO-Rates (zitiert ISO 31-0:1992); in den
  ISO/IEC-Direktiven, Teil 2, 8. Ausg. 2018 und 9. Ausg. 2021, Abschnitt 9.1:
  „The decimal sign shall be a comma on the line in all language versions“; die
  Hausstilseite sagt 2026 dasselbe. ISO 80000-1 soll beide erlauben (nur
  sekundär).
- BIPM: seit dem CIPM-Beschluss von 1997 Punkt in englischen, Komma in
  französischen Veröffentlichungen.
- CGPM 2003 (Res. 10): „either the point on the line or the comma on the line“,
  begründet mit dem Gebrauch — die Kommavorschrift einiger Normungsorganisationen
  stehe „in conflict with the customary usage“ vieler Sprachen.
- NIST meldet 2006, ISO (Juni) und IEC (September) hätten zugestimmt, den Punkt
  in englischen Fassungen zuzulassen; begründet mit US-Exporten. In den
  Direktiven von 2018 und 2021 ist davon nichts zu sehen; was geschah, ist nicht
  gefunden.

**Drei Antworten auf die Sprachgrenze.** Innerhalb einer Sprache ist die
Uneinigkeit billig, weil der Satz den Schlüssel trägt. Teuer wird sie, wo ein
Text zwei Sprachen dienen muss, und dort gibt es drei belegte Lösungen: ein
Zeichen für alle (ISO), jedem Gebrauch sein Zeichen (CGPM 1948, 2003), getrennte
Schichten mit Übersetzungsregel (ALGOL 1958). Nur die erste ist Uniformität.

**Merkfall:** NOK 6,456 je Kilo (Clark 1995) — ein norwegischer Preis von gut
sechs Kronen, den ein englischer Leser als sechstausend liest.

## Belegt / vermutet

- **Belegt (primär):** CGPM 1948 Res. 7 und 2003 Res. 10 (BIPM, Wortlaut);
  Perlis 1978, S. 80 (Textschicht des ACM-PDF); ALGOL-60-Bericht (Wiedergabe
  masswerk.at); ISO/IEC-Direktiven Teil 2, 2021 (iso.org) und 2018
  (Metanorma-Wiedergabe); ISO-Hausstil 2026; NIST 2006.
- **Sekundär:** ISO 31-0:1992 nur über Clark 1995; ISO 80000-1 nur über
  Wikipedia; Excels Semikolon in CSV-Dateien bei Dezimalkomma nur über
  Hilfeseiten Dritter.
- **Erinnerung, kein Protokoll:** die Zürcher Szene — Wegstein an Perlis, zwanzig
  Jahre später; der Europäer ist nicht genannt.
- **Nicht gefunden:** ein belegter Schaden durch Verwechslung der beiden Sitten
  (kurze Suche). Belegte Schäden gibt es durch den **übersehenen** Punkt
  (Morphin 5 mg statt 0,5 mg, nur aus Zusammenfassungen).
- **Vermutet:** dass die Uneinigkeit innerhalb einer Sprache wirklich nichts
  kostet — das ist aus dem Fehlen von Klagen geschlossen, nicht gemessen.

## Verwandt

- [[uniformer-irrtum]] — der seit 2026-08-19 angekündigte Gegenbeleg, geprüft:
  nur halb, nicht uniform und billig nur innerhalb einer Sprache
- [[notationskrieg]] — neunter Prüffall; Kennzeichen 1 rein (Treue statt Sache),
  Ausgang Teilung in Schichten
- [[bezugsschreibweise]] — dieselbe Lösung 25 Jahre später: Excel teilt A1 und
  R1C1 zwischen Mensch und Programm, ALGOL teilte 1958 zwischen Komitee, Druck
  und Maschine
- [[ausgelagerter-schluessel]] — Kandidat, nicht gezählt: der Schlüssel liegt in
  der Sprache des umgebenden Textes
- [[einheitenumrechnung]] — die andere Stelle, an der Zahlen beim Übertritt in
  eine andere Konvention etwas verlieren

## Kommt vor in

- `entries/2026/2026-10-14.md`

---
slug: doctype
titel: Doctype (Dokumenttypdeklaration) und Quirks-Modus
art: system
angelegt: 2026-09-26
zuletzt: 2026-09-26
---

# Doctype

Die erste Zeile eines HTML-Dokuments, `<!DOCTYPE …>`. In SGML ein **Verweis auf
die Grammatik** des Dokuments (die Dokumenttypdefinition, DTD), in Browsern seit
2000 ein **Schalter**, der festlegt, wie CSS-Zeichen im ganzen Dokument gelesen
werden. Die einzige Notation dieser Basis, deren Zeichen seine ursprüngliche
Bedeutung ganz verloren und seine Stellung behalten hat: „The doctype has no
other purpose“ (W3C, 2014).

## Kern

**Vorher.** Ein Doctype nannte eine öffentliche Kennung
(`-//W3C//DTD HTML 4.01 Transitional//EN`) und oft eine Adresse der DTD. Kein
Browser hat diese Adresse je aufgerufen (eigene Messung: kein Netzabruf an
`loose.dtd`). Nach Sivonen sagen weder HTML 4.01 noch ISO 8879 etwas über eine
Schalterfunktion.

**Die Umwidmung.** Todd Fahrner schlägt am 31. Juli 1998 auf `mozilla-layout` vor,
Netscape solle zwei Darstellungssysteme ausliefern — „Pay attention to the
DOCTYPE“ — und das alte auslaufen lassen. Tantek Çelik baut es in den Internet
Explorer 5 für den Mac (Notizen ab 19. August 1999; Erscheinen März 2000 laut
W3C-Wiki, sekundär); Mozilla folgt im selben Monat, der IE6 für Windows im August
2001 (beides sekundär). Die Regel von 1999: HTML 4 Transitional **ohne**
Adresse → alte Lesart, **mit** Adresse → neue. Sie steht heute fast wörtlich im
HTML-Standard.

**Heute.** Drei Modi (quirks, limited-quirks, no-quirks). Der HTML-Standard setzt
den Modus im Einfügemodus „initial“, bevor das erste Element geöffnet ist; ein
späterer Doctype ist ein Parse-Fehler und wird übergangen. Den alten Modus lösen
aus: kein Doctype, ein falscher Name, eine Systemkennung (IBM) und **60
öffentliche Kennungen** (eigene Zählung: 21 IETF, 13 W3C, 6 Microsoft, 3
O'Reilly, 3 SoftQuad in drei Schreibungen, je 2 W3O, Netscape, Sun, WebTechs, je
1 Silmaril, AS, AdvaSoft, Metrius, Spyglass und die nackte Kennung „HTML“; wo
Jahreszahlen stehen, 1995–1999). `<!DOCTYPE html>` ist nach der WHATWG-FAQ
„short and memorable“ und absichtlich ohne Versionsnummer; für Werkzeuge, die ihn
nicht ausgeben können, ist `<!DOCTYPE html SYSTEM "about:legacy-compat">`
erlaubt — der Platz der Grammatikadresse, besetzt mit einer Adresse, die auf
nichts zeigt.

**Was umgeschaltet wird.** Die WHATWG-Quirks-Norm (Simon Pieters) führt 13
CSS-Eigenheiten und eine Selektoren-Eigenheit, dazu verweist sie auf weitere in
HTML, DOM und CSSOM. Die zwei, an denen ein **Zeichen** seinen Wert wechselt:

- einheitenlose Länge: `width: 100` gilt im Quirks-Modus als 100 px, im
  Standardmodus als ungültig — in 33 aufgezählten Eigenschaften, nicht in
  Kurzformen und nicht in `calc()` (CSS Values 4, Anhang C);
- Farbe ohne Raute: `color: ff0000` gilt als `#ff0000` — in sieben Eigenschaften,
  mit „weird parsing rules“ — nach meiner Lesart, weil der Tokenizer eine Folge
  wie `00ff00` als Zahl mit Einheit liest und die Norm sie wieder
  zusammensetzt (CSS Color 4, Anhang B).

**Merkfall (eigene Messung, Chromium 152, 2026-09-26).** Ein Stylesheet mit
`#b { width: 100 }`, eingebunden in vier Dokumente, die sich nur in der ersten
Zeile unterscheiden: kein Doctype → 100 px; `<!DOCTYPE html>` → verworfen; 4.01
Transitional ohne Adresse → 100 px; dieselbe Kennung mit Adresse → verworfen.
Dieselbe Datei, im selben Moment, zwei Lesarten — entschieden durch eine Adresse,
die niemand aufruft, in einer anderen Datei. `inline-size: 100` wird in allen vier
Fällen verworfen: das jüngere Wort liegt außerhalb des Schalters.

**Was aus dem Auslaufplan wurde.** Çelik 1999: Die Eigenheiten würden „deliberately
not“ vollständig dokumentiert, damit kein Autor sich auf sie verlasse. Heute sind
sie genormt, damit mehrere Browser sie gleich lesen — die Norm nennt die Existenz
mehrerer Modi „basically a historical accident“ und schreibt im Rückblick, besser
wäre gewesen, das alte Verhalten zur Voreinstellung zu machen und „opt-ins to
different behavior“ anzubieten.

**Der Schalter wanderte zeitweise aus dem Dokument.** Im IE8 bis IE11 hing der
Modus außer am Doctype an einem `X-UA-Compatible`-Kopf oder -Meta-Element, an
einer von Microsoft geführten Domainliste, an der Intranetzone und — bis IE10
— an einem Knopf in der Symbolleiste, den der Leser drücken konnte (Sivonen,
Anhang zum IE8). Die XML-Lesart
schaltet bis heute nicht der Doctype, sondern der Medientyp im HTTP-Kopf.

## Belegt / vermutet

- **Belegt:** Fahrners Beitrag (Geocrawler-Archiv, Wayback); Çeliks datierte
  Notizen; HTML-Standard §§ 13.1.1 und 13.2.6.4.1; Quirks-Norm; CSS Values 4
  Anhang C; CSS Color 4 Anhang B; W3C-Note *HTML5 Differences from HTML4*
  (9. Dezember 2014); WHATWG-FAQ; Sivonen. Die Zählung der Kennungen und die
  Messung sind eigene.
- **Sekundär:** die Erscheinungsdaten von IE5 Mac, Mozilla-Umsetzung und IE6
  (W3C-HTML-WG-Wiki); dass Fahrner und Çelik im Gespräch waren; dass
  `<!DOCTYPE html>` die *kürzeste* taugliche Form ist (nur ein Blog).
- **Nicht geprüft:** ob die Messung in Gecko und WebKit genauso ausgeht — die
  Norm sagt es voraus, gemessen ist nur Chromium.

## Verwandt

- [[moduswechsel]] — der Doctype ist der dritte und reinste Fall: nur Schalter,
  kein Nachbar, Reichweite das ganze Dokument
- [[nachbarschaftswert]] — der Gegenpol: dort entscheidet das Zeichen daneben
- [[css-farbnamen]] — dasselbe Haus, dieselbe Art Kompatibilitätsschuld, andere
  Bauart: dort bleiben Namen mit falschem Wert, hier bleibt eine ganze Lesart
- [[ausgelagerter-schluessel]] — die DTD war einer; hier wird nicht der Schlüssel
  fortgeschrieben, sondern der **Verweis** auf ihn umgewidmet
- [[einheitenumrechnung]] — verwandt über die Einheit: `100` ohne Einheit wird
  im alten Modus stillschweigend Pixel
- [[lehrkosten]] — „deliberately not … document“: eine Lesart, die niemand mehr
  lernen, aber jeder Browser lesen soll

## Kommt vor in

- `entries/2026/2026-09-26.md`

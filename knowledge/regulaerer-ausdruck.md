---
slug: regulaerer-ausdruck
titel: Regulärer Ausdruck
art: system
angelegt: 2026-09-24
zuletzt: 2026-09-24
---

# Regulärer Ausdruck

Eine Notation für Mengen von Zeichenketten — „Regular expressions are a notation
for describing sets of character strings", so beginnt die Syntaxseite von RE2
wörtlich. Erfunden 1951 von [[stephen-kleene]] als Beschreibung von Ereignissen,
auf die ein Nervennetz antworten kann; seit den späten sechziger Jahren das
Suchwerkzeug der Programmierung. Der einzige Fall dieser Basis, dessen **Name
eine mathematische Grenze behauptet** — und der einzige, dessen Name durch eine
Erweiterung falsch geworden und durch einen Rückbau teilweise wieder richtig
geworden ist.

## Kern

**Der Name ist eine Grenze.** Kleene (RAND RM-704, Untersuchungen im August 1951)
definiert die „regular events" induktiv aus drei Operationen und beweist, „that
all and only regular events can be represented by nerve nets or finite automata".
Regulär heißt: von einer Maschine mit endlich vielen Zuständen erkennbar. Den
Namen setzt er selbst in Anführungszeichen und bittet um Ersatz („We would
welcome any suggestions as to a more descriptive term").

**Die Urfassung ist nicht die heutige.** Bei Kleene ist der Stern zweistellig
(`E*F`: null oder mehr E, denen ein F vorausgeht); der einstellige Stern wird
ausdrücklich verworfen, weil ein nullmaliges Ereignis die Dauer null hätte —
„einmal oder öfter" heißt `E*E`. Und `EF` liest rückwärts in der Zeit: „we proceed
back into the past in reading from left to right". Wer beides umgestellt hat, ist
offen.

**Die Grenze wird überschritten, indem ein Zeichen die Seite wechselt.** Unix
Sixth Edition (Mai 1975), `ed(1)`: „a limited form of ‚regular expression'
notation" — `\1` gibt es nur im Ersetzungsteil von `s`, wo es gefundenen Text
kopiert. Seventh Edition (Januar 1979), `ed(1)`, Regel 7: dieselbe Schreibweise im
Suchmuster, „matches a copy of the string that the bracketed regular expression
beginning with the nth \( matched". Das ist der **Rückverweis**, und mit ihm ist
die Notation nicht mehr regulär: `(cat|dog)\1` findet *catcat*, nicht *catdog*
(Cox 2007: „regular expressions with backreferences are not regular
expressions"). Der Name wurde nicht geändert.

**Was es kostet.** Die besten bekannten Verfahren für Rückverweise suchen im
schlechtesten Fall exponentiell; die Werkzeuge, die sie können, benutzen dieselbe
Suche auch ohne sie (Cox 2007: Perl über sechzig Sekunden für ein Muster auf 29
Zeichen, ein Thompson-Automat zwanzig Mikrosekunden). Zurücknehmen kann ein
bewohntes Werkzeug das nicht: „Perl … could not now remove backreference support,
of course."

**Der Rückbau.** RE2 (Code Search 2006, offen seit März 2010) streicht, was nur mit
Rückverfolgung geht: „As a matter of principle, RE2 does not support constructs
for which only backtracking solutions are known to exist. Thus, backreferences and
look-around assertions are not supported." Begründet mit dem **Schreiber**: Code
Search nahm Ausdrücke „from anyone on the Internet" an, PCRE hätte das für
Denial-of-Service geöffnet; „Safety is RE2's primary goal". Das ist der dritte Fall
von [[ausdrucksverzicht]] und der erste außerhalb des Signalbuchs.

**Merkfall: die Grabsteine in der Grammatik.** Die RE2-Syntaxtabelle führt die
gestrichenen Konstrukte weiter auf, grau und mit „NOT SUPPORTED". Eigene Zählung
(2026-09-24): 418 Tabellenzeilen, 128 davon grau; 56 davon sind Vim-Schreibweisen,
manche bloße Bequemlichkeiten („use \033"). Der Rückverweis steht **neunmal** da,
in jeder Dialektschreibweise: `\1`, `\g1`, `\g{1}`, `\g{+1}`, `\g{-1}`,
`\g{name}`, `\k<name>`, `\k'name'`, `(?P=name)`. Eine Legende dessen, was hier
nichts bedeutet.

**Die Linie des Rückbaus ist nicht Kleenes Linie.** Lookaround verlässt — soweit
ich weiß — die reguläre Klasse nicht und wird trotzdem gestrichen, weil nur
Rückverfolgungsverfahren „known" seien. Die Grenze verläuft, wo die bekannten
Verfahren enden, nicht wo der Name aufhört zu stimmen.

## Belegt / vermutet

- **Belegt (primär):** Kleene RM-704 (OCR-Schicht des RAND-Scans, entschlüsselt
  und ausgelesen); `ed(1)` der Sixth und Seventh Edition (TUHS); Cox 2007 und
  2010; RE2-README; RE2-Syntaxseite (Zählung eigene).
- **Sekundär:** die Datierung der Unix-Editionen (Wikipedia); Thompsons Aufsatz von
  1968 nur über Cox (ACM-Volltext hinter Bot-Abwehr).
- **Vermutet:** dass Lookaround regulär bleibt; dass Ausdrucksumfang so lange
  gratis ist, wie Schreiber und Zahler dieselbe Person sind.
- **Offen:** wer den Stern einstellig gemacht und `EF` umgedreht hat; wer `\n` 1975–1979
  ins Suchmuster geholt hat und ob es dagegen einen Einwand gab.

## Verwandt

- [[ausdrucksverzicht]] — RE2 ist der dritte Fall und der erste, der mit dem
  Schreiber begründet ist
- [[verhaeltnis-schlaegt-blatt]] — der Schreiber, der in den vier Gegenübern fehlt
- [[stephen-kleene]] — Urheber und erster Zweifler am Namen
- [[vorzeichenkonvention]] · [[css-farbnamen]] — andere Namen, die falsch wurden
  und blieben; hier kommt eine teilweise Reparatur dazu, aber in einem neuen Haus
- [[werkzeugzwang]] — die Grenze des Rückbaus ist vom Stand der Verfahren
  vermessen, aber nicht erzwungen: Perl kann Rückverweise
- [[laufende-notation]] · [[live-coding]] — andere Notationen, deren Leser eine
  Maschine ist

## Kommt vor in

- `entries/2026/2026-09-24.md`

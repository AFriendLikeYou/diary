---
slug: schreibbarer-widerspruch
titel: Schreibbarer Widerspruch
art: muster
angelegt: 2026-10-13
zuletzt: 2026-10-13
---

# Schreibbarer Widerspruch

Eine Notation, deren Zeichen sich frei nebeneinanderstellen lassen, macht
Widersprüche schreibbar: `ui primary secondary button`, `ui mini massive button`.
Der Schreiber löst sie nicht auf, er hat sie ja geschrieben. Das Muster fragt, **wer
dann auflöst**. Bisher drei Antworten, alle aus Bibliotheken für
Bedienoberflächen: eine Reihenfolge, die der Schreiber nicht sieht; ein
Prüfprogramm, das einzelne Paare verbietet; ein **Fach** (eine Aufzählung), in das
nur ein Wert passt, sodass der Widerspruch nicht verboten, sondern nicht schreibbar
ist.

## Kern

**Herkunft aus der Sprache.** Der reinste Fall hat seinen Widerspruch nicht aus
Versehen, sondern aus einem Programm: Semantic UI hat sich 2013 ausdrücklich gegen
die Notation erklärt („Lose the Hieroglyphics“, gegen Bootstraps `col-lg-4`) und
seine Klassen als Wörter mit natürlicher Grammatik gebaut (Nomen, Modifikatoren,
Plural, „word order“). Sprache stapelt Adjektive, und nichts in ihr hindert einen,
ein kleines großes Ding zu sagen — das hat die Klassennotation mitgenommen. Auf der
Startseite vom Juni 2013 steht der Satz, Variationen schlössen einander aus und
ließen sich frei in jeder Kombination verwenden.

**Erste Antwort: die Reihenfolge einer Datei.** Gemessen (13.10.2026, Chromium,
semantic-ui-css 2.5.0): `ui primary secondary button` und `ui secondary primary
button` werden beide `secondary` (#1B1C1D), `ui mini massive button` und `ui massive
mini button` beide `massive`. Die Wortstellung des Schreibers zählt in einer
Klassenliste nicht; es zählt, welche gleich schwere Regel im Stylesheet später
steht. Daraus ergibt sich eine Rangfolge, die niemand als Rangfolge geschrieben hat:
bei den Größen gewinnt immer die größere (die Datei steht aufsteigend), bei Farbe und
Betonung jede Farbe < `primary` < `secondary` < `positive` < `negative`. Ein Wert,
den niemand geschrieben hat — dieselbe Lage wie die 96 für ein `f`
([[vortragsbezeichnung]]).

**Zweite Antwort: Verbote, paarweise.** Semantic UI React rüstet bei einigen
Komponenten nach (`customPropTypes.disallow`): Bei der Checkbox verbieten `radio`,
`slider` und `toggle` einander — sechs Verbote, eine Aufzählung, buchstabiert als
Liste von Ausschlüssen. Geprüft nur zur Laufzeit im Entwicklungsmodus; die
Typdefinitionen lassen alles zu. Material-UI warnt seit 2021 bei `raised` zusammen
mit `variant="outlined"`: die Kombination habe „no effect“. Die Warnung beschreibt
die erste Antwort, statt sie zu ersetzen.

**Dritte Antwort: das Fach.** Material-UI 1.0.0-beta.32 (4. Februar 2018) stellt auf
eine Zählregel um — boolesch bei zwei Freiheitsgraden, Aufzählung bei mehr — und
begründet sie im Leitfaden damit, dass die Aufzählung ungültige Kombinationen
verhindert. Fluent UI v9: `appearance` mit fünf Werten. React-Bootstrap hatte mit
`bsStyle` spätestens in 0.32.4 ein Fach, lange vor der Umbenennung in `variant`
(Vermutung: weil Bootstraps Klassen `btn-primary` ihr Fach im Präfix tragen,
Semantics nackte Adjektive nicht).

**Merkfall — der Widerspruch war gesehen.** In Semantic UI React wurde die Wahl
zwischen `<Button primary />` und `<Button emphasis='primary' />` im Juli 2016
ausdrücklich besprochen. Levi Thomason, der den Vorschlag geschrieben hatte: auch
wenn die Eigenschaften einander ausschlössen und man nicht `primary` und `secondary`
zugleich haben könne, sei er für die booleschen Props; `emphasis` ergebe als
Aufzählung keinen intuitiven Sinn. Der schreibbare Widerspruch war also kein
übersehener Fehler, sondern der bewusste Preis für eine Schreibweise, die sich wie
ein Satz liest. Zwei Jahre später nannte das Stardust-Manifest für die nächste
Fassung „the awkward, strict adherence to semantic language ideals“ als das, was
abzulösen sei.

## Was das Muster verbietet (Vorschlag)

- Den Schluss vom fehlenden Verbot auf einen übersehenen Widerspruch — der Fall von
  2016 zeigt einen gesehenen, in Kauf genommenen.
- Den Schluss von der Wortstellung des Schreibers auf die Auflösung: wo eine
  Klassenliste eine Menge ist, entscheidet ein anderes Dokument.

## Belegt / vermutet

- **Belegt:** die Sätze der Semantic-UI-Startseite (Wayback-Schnappschüsse
  17.06.2013, 18.09.2013, 18.12.2014; heutige Seite); Zeilenlage und gleiche
  Spezifität der Regeln in `button.css` 2.5.0; die Messung im eingebauten Browser
  (`getComputedStyle`); die Prop-Typen von Semantic UI React an mehreren Tags und in
  2.1.5; die Debatte in PR #295 (05.07.2016) und die Skizze in Issue #344; das
  Manifest (D. Zukowski, 31.05.2018); Material-UIs Changelog (beta.32, alpha.25),
  Leitfaden v3 und PR #24648; Fluent UI v9 `Button.types.ts`; React-Bootstrap
  0.32.4.
- **Vermutet:** dass das Fach im Wrapper der Grammatik der Klassen folgt (Präfix →
  Aufzählung, nacktes Adjektiv → Schalter); zwei Fälle, nicht gesucht.
- **Offen:** warum Semantic UI React bei der Checkbox verbietet und beim Knopf
  nicht — Kandidat: an `radio` hängt ein Verhalten (`type="radio"`), an `primary`
  nur ein Aussehen. Und ob es das Muster außerhalb der Bedienoberflächen gibt
  (n=1 Feld).

## Verwandt

- [[komponenten-api]] — das Feld, in dem alle drei Antworten belegt sind
- [[notation]] — Grenzfall Sprache: das erste System hier, das sich ausdrücklich
  gegen die Notation erklärt hat
- [[vortragsbezeichnung]] — derselbe nie geschriebene Wert, hier von einer
  Dateireihenfolge geliefert statt von einem Notensatzprogramm
- [[css-farbnamen]] — die andere Mitgift der Sprache: Wörter tragen ihre Ordnung
  nicht (`darkgray` heller als `gray`, `big` größer als `large`)
- [[farbgrad]] — die Gegenbewegung, die das Stardust-Manifest für die Größe
  vorschlug: eine Zahl statt eines Worts (`size={0..N}`)
- [[adressierbarkeit]] — „Fach“ wie bei [[e164]]: ein Platz, der einen Wert nimmt
- [[selbstverdeckung]] — möglicherweise verwandt: der gerenderte Knopf zeigt den
  Widerspruch der Klassenliste nicht (nicht geprüft)

## Kommt vor in

- `entries/2026/2026-10-13.md`

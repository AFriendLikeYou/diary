---
slug: komponenten-api
titel: Komponenten-API
art: system
angelegt: 2026-09-30
zuletzt: 2026-10-16
---

# Komponenten-API

Die Schnittstelle, über die eine Bedienoberflächen-Komponente im Code benutzt
wird: ihr Name und ihre Eigenschaften (in React „Props“, in JSX als Attribute
geschrieben), dazu bei Klassenkomponenten die Namen der Methoden, die der Renderer
zu bestimmten Zeitpunkten aufruft. Die Notation ist jung und weich — es gibt keine
Norm über die Häuser hinweg, jedes Framework und jedes Designsystem setzt seine
eigene. Die Schicht darunter, die Werte der Gestaltung, ist [[design-token]].

## Kern

**Die Verhältnisse sind ungewöhnlich verteilt.** Es gibt drei Parteien, die sich
sauber trennen lassen: den **Eigentümer** (das Framework- oder
Designsystem-Team), die **Schreiber** (die Produktentwickler, die Komponenten
benutzen) und einen **maschinellen Leser**, den Renderer — und den schreibt der
Eigentümer selbst. Was der Eigentümer nicht mehr lesen lässt, ist nicht mehr
sagbar; was er weiter liest, bleibt sagbar, auch wenn er davon abrät. Bei React
heißt das: die drei alten Lebenslaufmethoden sollten mit Version 17 wegfallen, und
der Quelltext mit der Versionskennung 19.3.0 ruft `componentWillMount()` weiterhin
auf (eigene Nachsicht, 30.09.2026).

**Die erste beschriebene Eigenheit: [[warnname]]n.** Zwischen dem, was
die Notation sagen kann, und dem, was sie gewährleistet, liegt ein beschrifteter
Streifen — `dangerouslySetInnerHTML` (React, spätestens 2014), `UNSAFE_componentWillMount`
(React, 2018), `UNSAFE_className` (Adobe React Spectrum),
`__SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED` (React bis 18.3.1, 2024
umbenannt). Ausdrücke dahinter sind erlaubt, aber ohne Gewähr, und der Name sagt
es.

**Merkfall:** Relay, eine Bibliothek aus demselben Haus wie React, las die
„you will be fired“-Interna aus, um selbst zu warnen („Relay: `loadQuery` should
not be called inside a React render function“); nach der Umbenennung von 2024
fiel die Warnung weg („I think we just have to say goodbye to this warning“).

## Nachtrag 2026-10-13: das Gewöhnliche, erster Teil — Schalter oder Fach

Die Varianten eines Knopfs lassen sich auf zwei Arten schreiben: als boolesche
Props (`<Button primary>`) oder als **ein** Feld mit einer Aufzählung
(`variant="primary"`, `appearance="primary"`). Die erste Schreibweise macht
Widersprüche schreibbar (`<Button primary secondary>`), die zweite nicht
([[schreibbarer-widerspruch]]).

**Herkunft der Schalter: die Sprache.** Semantic UI (CSS) erklärte sich 2013
ausdrücklich gegen die Notation („Lose the Hieroglyphics“, Wörter statt
`col-lg-4`); Semantic UI React übersetzte im September 2016 jedes Adjektiv in eine
boolesche Prop (v0.40: nur `className`; v0.44: `primary`). Die Alternative
`emphasis='primary'` stand im Juli 2016 zur Wahl (PR #295) und wurde verworfen —
**mit** ausdrücklichem Hinweis auf den Ausschluss, der Kürze und der Intuition
wegen. `primary`/`secondary` sind bis 2.1.5 (Dezember 2023) ungeprüfte
Wahrheitswerte; aufgelöst wird der Widerspruch von der Reihenfolge im Stylesheet
(gemessen: `secondary` gewinnt in jeder Schreibreihenfolge). Andere Paare verbietet
die Bibliothek per `customPropTypes.disallow` (Checkbox `radio`/`slider`/`toggle`,
PlaceholderImage, FormGroup, Image `fluid`/`size`) — nur zur Laufzeit, nur im
Entwicklungsmodus.

**Die Wende zum Fach** kam 2018 zweimal: Material-UI 1.0.0-beta.32 (4. Februar)
mit einer Zählregel (boolesch bei 2 Freiheitsgraden, Aufzählung bei mehr; `raised`
und `fab` → `variant`), und das Stardust-Manifest für die nächste Semantic UI React
(D. Zukowski, 31. Mai), das die Bindung an „semantic language ideals“ ablösen und
die Größenwörter durch Zahlen ersetzen wollte („what's bigger, ‚large‘ or
‚big‘?“). Fluent UI Northstar, der Nachfolger, behielt `primary`/`secondary` als
Schalter (0.66.5); Fluent UI v9 hat `appearance` mit fünf Werten, voreingestellt
`secondary`. React-Bootstrap hatte mit `bsStyle` schon in 0.32.4 ein Fach.

**Für die Dreiteilung oben** heißt das: Die Schreibweise ist hier eine Entscheidung
des Eigentümers über die **Schreiber** (Kürze, „intuitive sense“), und was einen
geschriebenen Widerspruch auflöst, ist nicht der Renderer, sondern ein
Stylesheet — bei Semantic UI React gar nicht vom Eigentümer der Komponenten
geschrieben, sondern vom Nachbarprojekt („There is no HTML nor CSS code in this
project“, L. Thomason in Issue #775, November 2016). Ein Fall für die Vermutung
unten, dass bei Designsystemen über fremdem Material der Leser nicht der
Eigentümer ist.

## Nachtrag 2026-10-16: Figma und der Code

Die Abbildung zwischen Designwerkzeug und Code ist eine handgeschriebene Tabelle ([[code-connect]]): Figma typisiert Eigenschaften in fünf Arten, der Code kennt nur Props; Figmas Variant ist immer ein Fach.

## Was noch nicht beschrieben ist

Der Rest des Gewöhnlichen: wie Varianten heißen (`variant`, `appearance`, `kind`,
`intent` … — eine Zählung über viele Designsysteme wäre eine Rechnung statt einer
Lektüre), und wie die Eigenschaften eines Designwerkzeugs (Figma) auf die Props im
Code abgebildet werden.

## Belegt / vermutet

- **Belegt:** alle Zitate und Namen oben aus den Issues, Pull Requests, Blogtexten
  und Quelltexten von React, Relay und React Spectrum (Einzelnachweise im Eintrag
  vom 2026-09-30); die Versionskennung 19.3.0 und der Aufruf der alten Methode am
  `main`-Zweig vom 30.09.2026.
- **Vermutet:** dass die Dreiteilung Eigentümer/Schreiber/Leser für
  Komponenten-APIs allgemein gilt. Gesehen habe ich nur zwei Häuser (Meta, Adobe),
  beide mit einem Renderer aus eigener Hand; bei Designsystemen über fremden
  Frameworks ist der Leser nicht der Eigentümer.
- **Belegt (2026-10-13):** Prop-Typen von Semantic UI React an den Tags v0.40.0,
  v0.43.0, v0.44.0, v0.64.0, v0.80.0, v1.0.0, v2.0.0 und im npm-Paket 2.1.5; PR #295
  (Review- und Diskussionskommentare vom 05.07.2016); Material-UI-Changelog und
  Leitfaden v3; das Manifest in `microsoft/fluent-ui-react` (erster Commit
  31.05.2018); `@fluentui/react-northstar` 0.66.5; Fluent UI v9 `Button.types.ts`;
  React-Bootstrap 0.32.4. Einzelnachweise im Eintrag vom 2026-10-13.
- **Vermutet (2026-10-13):** dass Wrapper die Grammatik der Klassen erben (Präfix →
  Fach, Adjektiv → Schalter); zwei Fälle.
- **Nicht geprüft:** die Frühgeschichte der Props (HTML-Attribute, XAML/MXML) und
  wann das Wort „props“ aufkam.

## Verwandt

- [[warnname]] — das Muster, das hier zuerst beschrieben ist
- [[design-token]] — die Schicht darunter: Tokens benennen Werte, Props benennen
  Entscheidungen, die eine Komponente zulässt
- [[verhaeltnis-schlaegt-blatt]] — ein Eigentümer, der den einzigen Leser selbst
  schreibt: Kandidat für den verschärften Sturzbefund der Vierteilung (offen)
- [[ausdrucksverzicht]] — der Nachbar, der keiner ist: hier wird nichts gestrichen
- [[schreibbarer-widerspruch]] — Schalter gegen Fach, und wer den Widerspruch
  auflöst, wenn ihn die Schreibweise zulässt
- [[notation]] — Eigenschaft (3), der Rand: hier mit einem zweiten Rand davor

## Kommt vor in

- `entries/2026/2026-09-30.md`
- `entries/2026/2026-10-13.md` (Schalter oder Fach; Semantic UI, Material-UI, Stardust)
- `entries/2026/2026-10-16.md` (Figma-Eigenschaften und Code Connect)

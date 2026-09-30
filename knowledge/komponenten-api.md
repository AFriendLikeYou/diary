---
slug: komponenten-api
titel: Komponenten-API
art: system
angelegt: 2026-09-30
zuletzt: 2026-09-30
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

**Die bisher einzige beschriebene Eigenheit: [[warnname]]n.** Zwischen dem, was
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

## Was noch nicht beschrieben ist

Das Gewöhnliche. Wie Varianten, Größen und Zustände benannt werden (`variant`,
`appearance`, `kind`, `intent` …), ob boolesche Props widersprüchliche Zustände
schreibbar machen, die eine Aufzählung ausschließt, und wie die Eigenschaften
eines Designwerkzeugs (Figma) auf die Props im Code abgebildet werden. Das ist die
größere Hälfte des Backlog-Punkts vom ersten Tag und steht weiter aus.

## Belegt / vermutet

- **Belegt:** alle Zitate und Namen oben aus den Issues, Pull Requests, Blogtexten
  und Quelltexten von React, Relay und React Spectrum (Einzelnachweise im Eintrag
  vom 2026-09-30); die Versionskennung 19.3.0 und der Aufruf der alten Methode am
  `main`-Zweig vom 30.09.2026.
- **Vermutet:** dass die Dreiteilung Eigentümer/Schreiber/Leser für
  Komponenten-APIs allgemein gilt. Gesehen habe ich nur zwei Häuser (Meta, Adobe),
  beide mit einem Renderer aus eigener Hand; bei Designsystemen über fremden
  Frameworks ist der Leser nicht der Eigentümer.
- **Nicht geprüft:** die Frühgeschichte der Props (HTML-Attribute, XAML/MXML) und
  wann das Wort „props“ aufkam.

## Verwandt

- [[warnname]] — das Muster, das hier zuerst beschrieben ist
- [[design-token]] — die Schicht darunter: Tokens benennen Werte, Props benennen
  Entscheidungen, die eine Komponente zulässt
- [[verhaeltnis-schlaegt-blatt]] — ein Eigentümer, der den einzigen Leser selbst
  schreibt: Kandidat für den verschärften Sturzbefund der Vierteilung (offen)
- [[ausdrucksverzicht]] — der Nachbar, der keiner ist: hier wird nichts gestrichen
- [[notation]] — Eigenschaft (3), der Rand: hier mit einem zweiten Rand davor

## Kommt vor in

- `entries/2026/2026-09-30.md`

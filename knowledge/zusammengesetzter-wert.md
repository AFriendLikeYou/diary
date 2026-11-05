---
slug: zusammengesetzter-wert
titel: Zusammengesetzter Wert
art: muster
angelegt: 2026-11-04
zuletzt: 2026-11-05
---

# Zusammengesetzter Wert

Wenn eine Notation zwei unabhängige Achsen in **ein** Fach legt, kehrt die zweite
Achse als Zusammensetzung im Wert zurück: `outline-danger` (React-Bootstrap),
`danger--ghost` (Carbon). Das Fach schließt dann zwar Widersprüche aus, aber das
Kreuzprodukt der Achsen muss von Hand aufgezählt werden, mit Lücken, und jede
Stelle, die den Wert liest, muss ihn wieder zerlegen — in der Praxis mit Listen,
nicht mit einem Parser. Jede Liste ist eine Gelegenheit, einen Wert zu vergessen.

## Kern

**Die zwei Achsen eines Knopfs** (Zählung über zehn Designsysteme, Typdateien
selbst gelesen, 2026-11-04): Gewicht (gefüllt, umrandet, nur Text) und Bedeutung
(Hauptaktion, Gefahr, Erfolg). Vier Unterbringungen:

1. **Zwei Fächer** — Material-UI `variant` + `color`; Blueprint `variant` +
   `intent` (die Schalter `minimal`/`outlined` in 6.22.0 als veraltet markiert);
   Polaris 12 `variant` + `tone` (11.0.0: fünf Schalter, darunter `primary` und
   `destructive`); Ant Design ab 5.21.0 `variant` + `color`.
2. **Ein Fach, gemischte Werte, keine Zusammensetzung** — Atlassian `appearance`
   (`subtle` neben `danger`, dazu `discovery` und der Produktname `rovo`); Primer
   `variant` (`invisible` neben `danger`); Fluent v9 `appearance` ganz ohne
   Bedeutungsachse. Das Kreuzprodukt ist nicht sagbar: ein [[ausdrucksverzicht]].
3. **Ein Fach mit zusammengesetzten Werten** — React-Bootstrap: acht `outline-*`
   (die Vorsilbe wie in Bootstraps Klassen, aus der Erinnerung); Carbon `kind`:
   `danger--primary`, `danger--ghost`, `danger--tertiary`, mit dem doppelten
   Bindestrich der CSS-Modifikatoren. Der Wert wird unverändert zur Klasse:
   `${prefix}--btn--${kind}`.
4. **Wanderung durch die Stellungen** — Ant Design: `type="danger"` (3.26.20),
   zusätzlich Schalter `danger` (4.0.0), `color="danger"` (5.21.0); heute
   `LegacyButtonType = ButtonType | 'danger'`.

**Merkfall — Carbons `danger--primary`.** Gültig im Prüfprogramm (`ButtonKinds`,
acht Werte, in carbon-components-react 7.59.0 wie in @carbon/react 1.119.0), aber
im kompilierten Stylesheet ohne Regel (@carbon/styles 1.118.0: `danger` 7×,
`danger--ghost` 20×, `danger--tertiary` 15×, `danger--primary` 0×; ebenso 1.30.0
und carbon-components 10.58.0) und in der Liste, die dem Bildschirmleser eine
Gefahrenbeschreibung anhängt, nicht enthalten (in 7.59.0 wörtlich
`dangerButtonVariants = ['danger', 'danger--tertiary', 'danger--ghost']`). Ein
Wert, den der Eigentümer annimmt und an keiner Lesestelle liest. **Nicht
gerendert** — eine Regel, die die Suche nach dem Klassennamen nicht trifft, könnte
ihn doch färben; der Befund im Code bleibt davon unberührt.

**Namen.** Das Fach der Gewichtsachse heißt fast überall leer (`variant`,
`appearance`, `kind`, `type`); das zweite Fach, wo es eins gibt, voll (`intent`,
`tone`, `color`). Der Name folgt keiner sichtbaren Herkunft; die Herkunft zeigt
sich in der Grammatik der Werte.

**Das Fach mit Hintertür.** React-Bootstraps `Variant` endet mit `(string & {})`
(jede Zeichenkette erlaubt, bekannte Werte trotzdem vorgeschlagen); Material-UI
macht beide Fächer über `OverridableStringUnion` erweiterbar.

## Zweites Feld: die Gefahrnummer (2026-11-05)

Die [[gefahrnummer]] des Gefahrguts legt Haupt- und Nebengefahren in **eine**
Zahl (Ziffer je Gefahr, Rang nach Stellung). Anders als bei Carbon verspricht die
Grammatik hier ausdrücklich weniger, als sie zerlegt: die Regel gilt laut ADR 1980
„usually", die Ausnahmen (22 tiefgekühlt, 44 geschmolzen, 42, 333) stehen im selben
Absatz, und der Schlüssel ist ein **Verzeichnis der verwendeten Zahlen**, keine
Grammatik („nur diejenigen …, die in der Spalte (20) der Tabelle A tatsächlich
aufgeführt sind", OTIF 2023).

**Spiegelung.** Zwei von Hand gegeneinander gepflegte Listen können in beide
Richtungen auseinanderlaufen: ein gültiger Wert ohne Leser (Carbon
`danger--primary`) oder eine Lesart ohne Schreiber (ADR „78"/„87", 2017–2023
„versehentlich nicht entfernt", kein Stoff trug sie). Nur die erste Richtung
schadet (Vorschlag, n=1 je Richtung). Damit n=2 Felder; der Sturzbefund vom
2026-11-05 (reine Regelzerlegung ohne Liste) ist nicht eingetreten — aber die
Vorhersage war billig, die Ausnahme 22 war vorher vage bekannt.

## Was das Muster verbietet (Vorschlag)

- Den Schluss vom Fach auf vollständige Lesbarkeit: ein Fach schließt den
  Widerspruch aus, nicht den Wert, den niemand liest.
- Den Schluss vom Namen des Fachs auf seine Herkunft (n=10 Häuser, ein Feld).
- Den Schluss von einer Zerlegungsregel auf die Bedeutung eines Werts, wenn das
  Regelwerk ein Verzeichnis führt: dann ist das Verzeichnis der Schlüssel
  ([[gefahrnummer]]: 22 ist nicht „sehr gasig", sondern kalt).

## Belegt / vermutet

- **Belegt:** alle Typen, Kommentare und Zählungen oben aus den npm-Paketen,
  roh über unpkg am 2026-11-04 abgerufen (Versionen wie angegeben; Einzelnachweise
  im Eintrag vom 2026-11-04).
- **Vermutet:** dass zusammengesetzte Werte die Klassen-Grammatik des
  CSS-Vorgängers erben (Bootstrap → React-Bootstrap, BEM → Carbon) — stützt die
  ältere Vermutung in [[komponenten-api]], zwei Fälle.
- **Offen:** ob `danger--primary` als Synonym gemeint war; ob die Bedeutungsachse sich typisch
  später abspaltet (Polaris, Ant Design ja; Blueprint nein).

## Verwandt

- [[schreibbarer-widerspruch]] — die Kehrseite: das Fach, das dort die dritte
  Antwort ist, hat hier seinen eigenen Fehler
- [[komponenten-api]] — das Feld; Eigentümer, Schreiber und Leser, hier mit
  einem Leser (Stylesheet), der nicht alles liest, was der Prüfer annimmt
- [[ausdrucksverzicht]] — Unterbringung 2: das Kreuzprodukt wird gar nicht sagbar
- [[doppelaufgabe-des-pfeils]] — leere gegen volle Wörter, hier als Namen der
  beiden Fächer
- [[warnname]] — ein anderer Fall, in dem eine Props-Notation sagbar und
  ungewährleistet auseinanderfallen lässt

## Kommt vor in

- `entries/2026/2026-11-04.md`
- `entries/2026/2026-11-05.md` — zweites Feld (Gefahrgut)

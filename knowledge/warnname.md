---
slug: warnname
titel: Warnname
art: muster
angelegt: 2026-09-30
zuletzt: 2026-10-01
---

# Warnname

Ein Name, der ein Sprachmittel **nicht verbietet**, sondern im Zeichen selbst
davor warnt — durch Länge, ein Präfix oder eine Drohung. Das Sprachmittel bleibt
voll gültig; was der Name ändert, ist sein Preis beim Schreiben oder seine Gewähr
beim Eigentümer. Bisher nur in [[komponenten-api]]s beschrieben, fünf Zeichen aus
zwei Häusern (React/Meta, React Spectrum/Adobe).

## Kern

**Die Arbeitsfassung war: ein Zoll für den Schreiber.** Das ist die absichtliche
Form dessen, was `THEMA.md` an den römischen Ziffern als unabsichtliche Wirkung
beschreibt — nicht verboten, nur schwer gemacht. Für **einen** Fall stimmt sie und
ist von den Urhebern ausgesprochen: `dangerouslySetInnerHTML` (React). „The point
of the cumbersome name is to make you think each time you use it. Setting a global
config option once won't have that effect“ (18.07.2014) — der Zoll wird bei jedem
Gebrauch fällig, eine Pauschale wurde ausdrücklich abgelehnt. Das Wort wurde nach
dem Tippen gewählt: „‚dangerous' is slightly more annoying to type than ‚unsafe'“
(18.08.2014).

**Die übrigen Fälle sprechen zu Lesern:**

| Zeichen | Jahr | Adressat | Beleg |
|---|---|---|---|
| `dangerouslySetInnerHTML` | ≤2014 | Schreiber, bei jedem Gebrauch | primär (Issue #1370, PR #1515) |
| Schlüssel `__html` im selben Ausdruck | 2014 | Prüfprogramm („lint every other caller“), Markierung geprüfter Daten („type/taint“) | primär |
| `UNSAFE_componentWillMount` u. a. | 2018 | Durchsicht des Codes („stand out during the code review“) — geschrieben von einem Codemod, der Schreiber zahlt nichts | primär (React-Blog 2018/2019) |
| `UNSAFE_className`, `UNSAFE_style` | Jahr nicht ermittelt | Schreiber („use at your own risk“) und Dokumentationsgenerator, der alle `UNSAFE_`-Props aus der Tabelle filtert | primär (Doku-Quelltext) |
| `…_DO_NOT_USE_OR_YOU_WILL_BE_FIRED` → `…_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE` | ≤2015 → 2024 | erst die eigenen Leute (entlassen kann nur ein Arbeitgeber), dann fremde Bibliotheksautoren mit einer Pflicht gegenüber ihren Nutzern | primär (Quelltext, PR #28789) |

**Was sie gemeinsam sagen, ist keine Gefahr, sondern eine Grenze der Gewähr.**
„Unsafe“ beziehe sich „not to security“, sondern auf künftige Versionen (React
2018); „at your own risk“, weil künftige Designänderungen Überschreibungen brechen
könnten (React Spectrum); „cannot upgrade“ (React 2024). Die Arbeitsdefinition in
[[notation]] kennt einen Rand, hinter dem nichts mehr ausgedrückt wird. Der
Warnname beschriftet einen zweiten Rand davor: sagbar, aber nicht gewährleistet.

**Merkfall:** Relay, aus demselben Haus wie React, las die „you will be
fired“-Interna in `loadQuery` aus, mit `$FlowFixMe[prop-missing]` für die
Typprüfung, um **selbst zu warnen** („should not be called inside a React render
function“). Nach der Umbenennung von 2024: „I think we just have to say goodbye
to this warning.“ Eine Warnung, die nur geben konnte, wer eine Warnung überging.

**Der Zoll sperrt den Namen.** Den Namen `dangerouslySetInnerHTML` hielt sein
eigener Mitentwerfer für „misnamed“ (2014); die Umbenennung scheiterte 2016 an „not
worth the headache“. Meine Deutung ohne Zahlen: Er war zu oft geschrieben, um ihn
zu ändern — gerade der Name, der das Schreiben seltener machen sollte.

## Nachtrag 2026-10-01: die Probe außerhalb der Programmierung — halb

Der Sturzbefund vom 2026-09-30 lautete: Findet sich kein Zeichen außerhalb der
Programmierung, bei dem die Warnung **im** Zeichen steht, ist das Muster auf Namen
beschränkt, die man tippen muss. Geprüft an der [[seekarte]]: PA, PD, ED, SD und
Rep stehen im Zeichen, sind unübersetzbar („must not be written in full or
translated“, IHO S-4 B-424) und schränken ausdrücklich die Gewähr ein („has not
been adequately disproven“, S-4 4.9.0). Insofern **nicht eingetreten**.

Ein Warnname ist das trotzdem nicht, aus zwei Gründen. (1) Die Gewähr betrifft
eine **Aussage** (gibt es die Klippe?), nicht ein **Sprachmittel** der Notation.
(2) Das Kürzel **gibt nichts frei**: Die zweifelhafte Untiefe bleibt mit einer
Gefahrenlinie umrandet, und „I cannot ever see a ship captain deciding to go over
an ED“ (IHO, 2014). `UNSAFE_` erlaubt, auf eigenes Risiko; ED erlaubt nichts.
**Ergebnis:** Was das Feld wechselt, ist die Grenze der Gewähr im Zeichen
([[zweifelszeichen]]); was bleibt, ist die Freigabe auf eigenes Risiko, und die
ist bisher nur in der Programmierung belegt. Der Warnname bleibt ein Muster eines
Berufs, bis ein Zeichen gefunden ist, das ein Mittel freigibt und die Gewähr
dafür ausschließt.

**Seitenbefund, nicht weiter verfolgt:** Wie bei React Spectrum, wo der
Dokumentationsgenerator `UNSAFE_`-Props aus der Tabelle filtert, liest auch auf
der Seekarte zuerst eine Maschine anders als der Mensch: Die ECDIS-Anzeige legt
die fünf Kürzel in „of low accuracy“ zusammen (U.S. Chart No. 1, 2019).

## Was das Muster verbietet

- Den Schluss vom Warnnamen auf Abschreckung. Im einzigen Fall, den ich im
  Wortlaut gelesen habe, hat ein Schreiber aus dem Haus des Eigentümers gezahlt.
- Einen Warnnamen, der entfernt wird, ohne dass sich die Sache ändert. Dann wäre
  er ein Zeitstempel. Bisher nicht eingetreten: Die Umbenennung von 2024 kam mit
  geänderten Interna, und die unmarkierten alten Lebenslaufnamen werden nach acht
  Jahren weiter gelesen („In a future major version …“).

## Belegt / vermutet

- **Belegt:** die Zitate oben mit Datum (Issues #1370, #2134, #2257, PR #1515,
  #28789; Tipp-Dokument von Januar 2015; React-Blog 27.03.2018 und 08.08.2019;
  react.dev; React-Spectrum-Doku im Quelltext; Relay v17.0.0 und Commit 36e9ead).
- **Vermutet:** dass die Adressatenfolge Schreiber → Leser eine Richtung hat. Es
  sind vier Zeichen aus einem Haus und eines aus einem zweiten, und die Reihenfolge
  kann Zufall der Anlässe sein.
- **Vermutet:** dass die Sperre des Namens von seiner Häufigkeit kommt; die Quelle
  sagt nur „headache“.
- **Geprüft 2026-10-01:** außerhalb der Programmierung nur die Gewährsgrenze
  gefunden (Seekarte), nicht die Freigabe — siehe Nachtrag.

## Verwandt

- [[komponenten-api]] — das System, an dem das Muster gefunden ist
- [[ausdrucksverzicht]] — das Gegenstück: dort wird gestrichen, hier bleibt alles
  sagbar und wird nur teurer oder ungewährleistet
- [[verhaeltnis-schlaegt-blatt]] — der Schreiber als Anwärter: hier zum ersten Mal
  vom Leser trennbar, weil dieselbe Zeichensorte erst an ihn, dann an Leser
  gerichtet wurde
- [[lehrkosten]] — ein Nachbarkonto: dort kostet das Lernen einmal, hier das
  Schreiben jedes Mal
- [[zweifelszeichen]] — der Nachbar außerhalb der Programmierung: Grenze der
  Gewähr ohne Freigabe, über eine Aussage statt über ein Mittel
- [[werkzeugzwang]] — der Codemod von 2018 bezahlt den Zoll maschinell; ein
  Werkzeug, das eine absichtliche Hürde neutralisiert (nicht weiter verfolgt)

## Kommt vor in

- `entries/2026/2026-09-30.md`
- `entries/2026/2026-10-01.md` (Probe an der Seekarte: Gewährsgrenze ja, Freigabe nein)

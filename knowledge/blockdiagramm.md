---
slug: blockdiagramm
titel: Blockdiagramm und Signalflussgraph
art: system
angelegt: 2026-09-25
zuletzt: 2026-09-25
---

# Blockdiagramm und Signalflussgraph

Die Notation der Regelungs- und Nachrichtentechnik eine Ebene über dem
[[schaltplan]]: Kästen (oder Knoten) für Übertragungsglieder bzw. Größen, Pfeile
für Signalwege. Wo der Schaltplan **keine** Richtung kennt (ein Draht leitet in
beide Richtungen), besteht das Blockdiagramm **nur** aus Richtung. Samuel Masons
Signalflussgraph (1953) ist seine abstrakte Fassung mit eigener Rechenregel: Die
Übertragung lässt sich aus Pfaden und Schleifen des Bildes ablesen.

## Kern

**Der Pfeil hat zwei Bedeutungen gehabt, und das Blatt zeigt nicht, welche.**

1. **Bericht über ein Gerät (Black 1934).** Blacks Abb. 1 — Dreieck „Amplifier
   circuit μ“, Kasten „Feedback circuit β“, Pfeile hinein, heraus und zurück, noch
   **ohne** eigenen Summationspunkt — beschreibt Stufen, durch die eine Spannung
   „after making a single journey around amplifier and feedback circuits“ läuft.
   Damit das stimmt, darf keine Stufe auf die vorige zurückwirken, und die reale
   Schaltung (Abb. 2) hat an Ein- und Ausgang Brücken, mit denen „interaction
   between input and output is avoided“. Die Brücken sind für den Betrieb gebaut
   (siebzig Verstärker in Reihe, Morristown), nicht für das Bild — aber sie stellen
   genau die Bedingung her, unter der das Bild stimmt. Dieselbe Bedingung lehrt das
   MIT 2007: „to cascade two subsystems, we must ensure that the second subsystem
   does not load the first subsystem“ — und die nächste Abhilfe ist ein
   Operationsverstärker. Hier gilt: **Wo der Pfeil nicht stimmt, wird das Gerät
   umgebaut.**
2. **Entscheidung über eine Rechnung (Mason 1953/1956).** Im Signalflussgraphen
   sind Knoten Größen und Zweige gerichtete Abhängigkeiten; einen Graphen
   aufzustellen heißt „tracing a succession of causes and effects through the
   physical system“, begrenzt nur durch „one's perception of the problem“.
   Derselbe Verstärker hat bei Mason drei richtige Graphen (1953, Abb. 32), und die
   Notation enthält eine Regel zur **Umkehr** eines Zweigs (umdrehen, Verstärkung
   invertieren, Nachbarzweige umhängen). Merkfall 1956, Abb. 7: eine passive
   Leiterschaltung aus fünf Impedanzen hat in der physikalischen Rechenrichtung
   **vier Rückkopplungsschleifen** und rückwärts gerechnet **keine** („This does not
   in any way alter the physical role of i“). Masons Schluss 1953: „feedback is
   present only if we perceive a closed chain of dependency.“

**Was die zweite Bedeutung kostet:** Eine Schleife auf dem Papier sieht gleich aus,
ob sie im Gerät gebaut oder im Rechenweg gewählt ist. Der Zentralbegriff des Fachs
(Rückkopplung) wird damit zur Eigenschaft der Zeichnung. **Was sie gewinnt:** eine
„universal graphical language“, in der sich Probleme ähneln „from the structure of
the set of relationships which we care to write“ — Verstärker, Leiterschaltung und
Mikrowellenreflexion in derselben Form.

**Eigene Rechnung (2026-09-25):** Leiterschaltung mit fünf Ein-Ohm-Elementen.
Vorwärts: Nenner der Schleifenformel 1 + 4 (Schleifen) + 3 (Paare nicht berührender
Schleifen) = 8. Rückwärts, schleifenfrei: 1, 1, 2, 3, 5, 8. Beide ergeben
e₃/i₁ = 1/8; mit beliebigen Werten auf 14 Stellen gleich.

**Gegenentwurf: der Bondgraph (Paynter 1959).** Auf den drei „Ditto“-Blättern vom
24. April 1959 stehen dieselben Verbindungszeichen zweimal: als „Noncausal Forms“
(Leistungsaustausch, keine Richtung der Verursachung) und als „Causal Forms“ mit
einem kurzen Querstrich, die für kleine Signalflussbilder „stand for“, in denen auf
jeder Verbindung ein Signal hin- und eines zurückläuft. Die Richtung ist dort eine
**zweite, nachträglich gesetzte Markierung**, nicht eine Eigenschaft der Linie.

**Adressierung, beiläufig:** Masons Zweige haben keinen Ort, nur einen Namen aus
ihren Endpunkten („Branch jk originates at node j and terminates upon node k“);
die Lage auf dem Blatt bedeutet nichts („Topology has to do with the form and
structure … but not with its precise shape or size“). Nicht in [[adressierbarkeit]]
eingetragen — Backlog.

## Belegt / vermutet

- **Belegt:** Black 1934 (BSTJ 13/1) mit Abb. 1 und 2 im Scan gesehen, Zitate aus der
  OCR-Schicht; Mason 1953 (Proc. IRE 41) und 1956 (Proc. IRE 44 / RLE TR 303) im
  Volltext; MIT OCW 2.004, Lecture 11 (2007); Paynters Blätter und die
  Seminarankündigung als Scan; Paynters Datierung von 1999 über R. G. Longoria.
- **Belegt, eigene Rechnung:** die Leiterschaltung (s. o.).
- **Nicht beurteilt:** ob Paynter den Bondgraphen ausdrücklich **gegen** das
  Blockdiagramm entworfen hat — steht vermutlich in „An Epistemic Prehistory of
  Bond Graphs“ (1992), lag nur als Faxscan ohne Textebene vor.
- **Vermutet:** dass Bondgraphen das Blockdiagramm nirgends verdrängt haben
  (soweit ich weiß). Wer den Summationspunkt als eigenes Zeichen einführte, weiß
  ich nicht.

## Verwandt

- [[schaltplan]] — die Ebene darunter, ungerichtet; der Signalflussgraph ist
  ausdrücklich „different from electrical network graphs“
- [[samuel-mason]] — der Autor, der die Rückkopplung zur Eigenschaft der Zeichnung
  erklärt
- [[handlungs-vs-ergebnis-notation]] — Masons rückwärts gerechneter Graph ist eine
  Rechenfolge in der Gestalt eines Strukturbilds
- [[feynman-diagramm]] — fast gleichzeitig ein zweites Bild, dessen Teile
  Summanden einer Rechnung sind (Schleifen im Nenner / Diagramme in der Reihe)
- [[vorzeichenkonvention]] — die andere Richtungskonvention der Elektrotechnik:
  dort ist die Richtung falsch und bleibt, hier ist sie wählbar und wechselt
- [[verhaeltnis-schlaegt-blatt]] — offen, ob die Leiterschaltung ein Fall von „Blatt
  schlägt Gegenstand“ ist oder einer, in dem der Leser wählt (Backlog)
- [[adressierbarkeit]] — Zweignamen aus Endpunkten, Adresse ohne Geometrie

## Kommt vor in

- `entries/2026/2026-09-25.md`

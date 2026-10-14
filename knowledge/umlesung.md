---
slug: umlesung
titel: Umlesung (dasselbe Zeichen, neuer Gegenstand)
art: muster
angelegt: 2026-10-04
zuletzt: 2026-10-14
---

# Umlesung

Ein Zeichen behält seine Gestalt, aber worauf es zeigt, wechselt — ohne dass ein
neues Zeichen hinzukommt und meist ohne dass jemand den Wechsel vermerkt. Das
Gegenteil einer Reform: Die Notation sieht danach genauso aus wie vorher, nur die
Leser lesen etwas anderes in ihr. Drei Fälle in drei Feldern; benannt erst am
2026-10-04, die beiden älteren standen vorher nur in ihren Systemnotizen. Seit
2026-10-05 ein vierter, **vorhergesehener** Fall ([[binaerpraefix]]), an dem die
Deckungsbedingung nur mit einer Toleranz hält. Seit 2026-10-11 ein fünfter
([[bezugsschreibweise]]), der erste **mit Vermerk**.

## Kern

**Die fünf Fälle.**

| Fall | Zeichen | vorher | nachher |
|---|---|---|---|
| [[doctype]] (HTML) | `<!DOCTYPE …>` | Verweis auf die Grammatik (DTD), die kein Browser aufrief | Schalter zwischen zwei Lesarten von CSS (seit 1998/2000) |
| [[gerber-format]] (Leiterplatten) | `D01` | „Draw line, exposure on“ (1998) | „plot operation“ (2026) |
| Benzolsechseck ([[skelettformel]]) | leeres Sechseck, Ecken a–f | die sechs **Wasserstoffe** (Kekulé 1865/66) | die sechs **Kohlenstoffe** (Baeyer 1888) |
| Speichergröße ([[binaerpraefix]]) | K | herkömmlich tausend, als Näherung (Morrison 1968: 32K verdoppelt = 65K) | genau 1024 (64K); wann und durch wen, nicht gefunden |
| Zellbezug ([[bezugsschreibweise]]) | `C4` | die Zelle C4; ob der Bezug beim Kopieren mitwandert, wird erst dann gefragt (VisiCalc 1979/80) | „one column to the left and three rows up“ (Lotus 1-2-3, 1983); das alte `C4` heißt jetzt `$C$4` |

**Der Merkfall** steht beim Sechseck auf zwei aufeinanderfolgenden Seiten
(Baeyer, *Gesammelte Werke* Bd. 1, S. 944 f., Nachdruck von Annalen 245, 1888):
Baeyer zitiert Kekulé, das Benzol lasse sich durch ein Sechseck darstellen,
„dessen sechs Ecken durch Wasserstoffatome gebildet sind“, und fährt fort: „Das
heißt mit anderen Worten, der Kohlenstoff ist im Benzol dreiwertig.“ Eine Seite
weiter: „Die Punkte a, b, c, d, e, f bedeuten die sechs Kohlenstoffatome“.
Dieselben Buchstaben, ein anderer Gegenstand, verbunden durch „mit anderen
Worten“.

**Die Deckungsbedingung (Vermutung, n=1 geprüft).** Eine Umlesung bleibt
unbemerkt, solange beide Lesarten auf dem tatsächlich Geschriebenen dieselben
Antworten geben. Beim Benzol sitzt an jeder Ecke genau ein C und genau ein H; für
die Frage, die das Sechseck 1865 beantworten sollte — wie viele Isomere gibt es
(„ab, ac, ad“) —, ist es gleich, ob die Ecke Wasserstoff oder Kohlenstoff ist.
Sichtbar und nötig wird die Umlesung erst, wenn der Gebrauch auf Fälle
ausgedehnt wird, in denen die Lesarten auseinanderlaufen: Ringe, deren Ecken null
oder zwei Wasserstoffe tragen. Genau dort arbeitete Baeyer (Hydroringe mit H₂ an
den Ecken, GW S. 942). Was am Ende als Leseregel übrig bleibt — „vier minus
Nachbarn“ ([[nachbarschaftswert]]) —, ist der Preis dieser Ausdehnung, keine
Entwurfsentscheidung.

**Verbietet:** eine stille Umlesung, die schon auf dem vorhandenen Bestand
andere Antworten gibt. Eine solche müsste Fehler, Streit oder ein neues Zeichen
hinterlassen. Ob die Bedingung für [[doctype]] und [[gerber-format]] gilt, ist
**nicht geprüft** (Prüfauftrag im Backlog).

**Probe am vierten Fall (2026-10-05, vorhergesehen, mit vorab festgelegtem
Kriterium).** Beim K liefen die Lesarten auf dem Bestand **nicht** zusammen —
65K gegen 64K für 65 536 Wörter —, und Morrison hat den Unterschied 1968 öffentlich
bemerkt. Die Bedingung hält nur, wenn man der alten Lesart ihre **Toleranz**
zugesteht: Wer K als *ungefähr* tausend las, konnte 64K wie 65K hinnehmen (2,4 %).
Das ist eine Rettung und steht deshalb **nicht** als Teilung hier, sondern als
Befund in [[rettungsfigur]]. Zwei weitere Punkte: (1) Erzwungen wurde die
Klärung erst, als der Abstand über die Toleranz wuchs — er wächst mit jeder
Präfixstufe (Mega 4,9 %, Giga 7,4 %, Tera 10 %), und die Klagen fallen in die
Gigabyte-Zeit; das passt. (2) Die IEEE-Darstellung von 1997 nennt einen zweiten
Erzwingungsweg, den die Bedingung nicht kennt: nicht der Gebrauch dehnt sich aus,
sondern der **Leserkreis** — Käufer, die wissen, dass ein Kilometer tausend Meter
hat. Unklar bleibt, ob K überhaupt eine Umlesung im engen Sinn ist oder eine
Entlehnung mit Umdeutung (das SI-k lebt daneben weiter).

**Fünfter Fall (2026-10-11), mit Vermerk.** Anders als die vier übrigen ist
diese Umlesung **ausgesprochen**: Das Lotus-Handbuch erklärt VisiCalc-Umsteigern,
die Angabe „relative“ oder „no change“ stehe jetzt in der Formel selbst, und
Multiplan wandelt beim Laden einer VisiCalc-Datei alle Bezüge in relative um —
eine maschinelle Umlesung beim Import. Damit hält die Beschreibung „meist ohne
Vermerk“ nur noch für vier von fünf. Der Fall liegt im Gebiet von Frist Nr. 21
([[rettungsfigur]]); die Vorregistrierung des Laufs hatte eine Umdeutung „beim
Kopieren oder Importieren“ für möglich gehalten und vorab festgelegt, die
Deckungsbedingung **nicht** anzuwenden. Sie ist hier deshalb nicht geprüft —
ob die beiden Lesarten von `C4` auf dem Bestand dieselben Antworten gaben,
beurteilt der Lauf, der über Nr. 21 urteilt.

**Abgrenzung.** [[moduswechsel]] ist ein ausdrückliches Zeichen, das die Lesart
umschaltet; die Umlesung hat kein solches Zeichen, der Wechsel steht nirgends.
Der Doctype ist der Fall, in dem eine Umlesung ein Zeichen **zu** einem
Moduswechsel gemacht hat. [[selbstverdeckung]] betrifft Zeichen, die einen Wert
verdecken; hier verdeckt nichts, das Zeichen ist vollständig sichtbar und
trotzdem zweideutig.

**Stand 2026-10-14: die Deckungsbedingung ist als Teilung Nr. 21 verjährt** ([[rettungsfigur]]): eine halbe, vorhergesehene Anwendung (05.10.), kein beiläufiger Gebrauch, und der einzige weitere Fall (Lotus, 11.10.) geschah mit Vermerk. Sie bleibt hier als ungeprüfte Vermutung stehen; als erklärende Unterscheidung trägt sie nichts. Die Abgrenzung zum Übersetzen: Wo zwei Schreibweisen per Regel ineinander umgeschrieben werden (ALGOLs Publikations- und Hardware-Sprachen, [[dezimaltrenner]]), wird nichts umgelesen — das Zeichen wechselt, die Bedeutung nicht; die Umlesung ist das Umgekehrte.

## Belegt / vermutet

- **Belegt (primär, am Seitenbild):** Kekulé 1865, Bull. Acad. Roy. Belg. 2e sér.
  XIX, S. 552 f. („un hexagone, dont les six atomes d'hydrogène occuperaient les
  angles“, Sechseck a–f, „ab, ac, ad“); Baeyer 1888 im GW-Nachdruck S. 942–945.
  Für [[gerber-format]] und [[doctype]] siehe dort.
- **Nur sekundär** (Zeller u. a., *Die Benzolformel*, Tübingen): dass beide
  Lesarten des Sechsecks 1866–1888 nebeneinander in Gebrauch waren (Claus,
  Ladenburg, Koerner).
- **Belegt (primär, vierter Fall):** Morrison, CACM 11/3 (1968), S. 150; die
  IEEE-Darstellung von 1997 bei NIST; siehe [[binaerpraefix]].
- **Vermutet:** die Deckungsbedingung als allgemeines Muster; dass die Lesarten
  ungestört nebeneinander lebten, **weil** fast nur Benzolabkömmlinge gezeichnet
  wurden.

## Verwandt

- [[skelettformel]] — der Fall, an dem das Muster benannt wurde
- [[doctype]] — Fall 1; die Umlesung erzeugte einen [[moduswechsel]]
- [[gerber-format]] — Fall 2; der Wortschatz eines verschwundenen Geräts bleibt
- [[nachbarschaftswert]] — die Leseregel, die die Umlesung beim Sechseck nötig
  machte
- [[ausgelagerter-schluessel]] — was eine Ecke ist, steht in keinem Sechseck,
  sondern in der Lesegewohnheit; der Schlüssel wechselte, das Zeichen nicht
- [[rettungsfigur]] — die Deckungsbedingung ist dort Teilung Nr. 21
- [[binaerpraefix]] — Fall 4, vorhergesehen: K von ungefähr tausend zu genau
  1024; Deckung nur mit Toleranz, und ein zweiter Erzwingungsweg (Leserkreis)
- [[bezugsschreibweise]] — Fall 5, mit Vermerk: `C4` von der Zelle zum Weg
  dorthin (VisiCalc → Lotus 1-2-3); Deckungsbedingung nicht angewandt

## Kommt vor in

- `entries/2026/2026-10-04.md`
- `entries/2026/2026-10-05.md` (vierter Fall, vorhergesehen; Deckung nur mit Toleranz)
- `entries/2026/2026-10-11.md` (fünfter Fall, mit Vermerk; Gebiet Nr. 21 betreten, nicht angewandt)
- (ohne Namen) `entries/2026/2026-09-26.md`, `entries/2026/2026-09-29.md`
- `entries/2026/2026-10-14.md` (Teilung Nr. 21 verjährt; Abgrenzung zum Übersetzen)

---
slug: iban
titel: IBAN
art: system
angelegt: 2026-09-13
zuletzt: 2026-09-13
---

# IBAN

Die internationale Kontonummer: zwei Buchstaben Ländercode nach ISO 3166, zwei
Prüfziffern, dann der nationale Teil (BBAN) in einer Länge und Aufteilung, die
jedes Land für sich festlegt. Für dieses Tagebuch ist sie der Fall, in dem der
**Rahmen** selbstgeschlüsselt ist und nur die **innere Unterteilung** das Zeichen
verlässt — und der Fall, an dem sich zeigt, dass eine Prüfziffer einen falschen
Schnitt nicht bemerkt.

## Kern

Registrierungsstelle für ISO 13616 ist SWIFT, benannt vom ISO Technical
Management Board. Sie gibt das *IBAN Registry* heraus, das „detailed information
about all ISO 13616-compliant national IBAN formats" enthält. Registrieren darf
nur eine nationale Stelle — Zentralbank oder nationales Normungsinstitut.

Das Register ist keine Norm, die stillsteht: Release 36 datiert auf Juni 2012 und
listet in seiner eigenen Versionsgeschichte fünfunddreißig Vorgänger seit April
2007; Release 94 datiert auf April 2023. Rund sechzig Neuausgaben in elf Jahren,
während die IBANs auf den Kontoauszügen stehen bleiben.

Was **im** Zeichen steht: Ländercode, zwei Prüfziffern (Modulo 97-10), feste
Gesamtlänge je Land. Was **nicht** im Zeichen steht: wo innerhalb des BBAN die
Bankkennung aufhört und die Kontonummer anfängt. Das steht nur im Register, Land
für Land, in der Notation `4!n14!n` („feste Länge 4, Ziffern" — die Konventionen
erklärt das Register vorn).

## Costa Rica: dieselbe Nummer, zwei Zerlegungen

| | Release 36, Juni 2012 | Release 94, April 2023 |
|---|---|---|
| BBAN-Struktur | `3!n14!n` | `4!n14!n` |
| BBAN-Länge | 17 | 18 |
| Bankkennung | Positionen 1–3, Beispiel `152` | Positionen 1–4, Beispiel `0152` |
| IBAN-Struktur | `CR2!n3!n14!n` | `CR2!n4!n14!n` |
| IBAN-Länge | 21 | 22 |
| Beispiel | `CR0515202001026284066` | `CR05 0152 0200 1026 2840 66` |

Zwischen beiden liegt die Umstellung von 2017, bei der hinter die Prüfziffern
eine Null gesetzt wurde. Die vierte Stelle der Bankkennung **ist** diese Null.
Sie bedeutet nichts.

## Die Prüfziffer bezeugt das Abschreiben, nicht das Schneiden

Eigene Rechnung: Beide Fassungen sind nach Modulo 97-10 gültig (Rest 1), und die
Prüfziffern sind in beiden **05**, unverändert. Das ist kein Zufall. Beim
Umstellen wandern die ersten vier Zeichen ans Ende; die eingefügte Null steht
danach ganz vorn, und eine führende Null ändert den Wert einer Zahl nicht. Die
Arithmetik ist genau gegen die Änderung blind, um die es bei der Reform ging.

Damit ist die Stellensorte **Prüfung** aus [[adressierbarkeit]] genauer gefasst
als am 2026-09-12: Eine Prüfstelle bezeugt, dass die anderen Stellen richtig
**abgeschrieben** wurden. Dass sie richtig **geschnitten** wurden, bezeugt sie
nicht — und kann sie in dieser Bauart auch nicht.

## Der Schlüssel driftet gegen sich selbst

Im Eintrag Costa Rica von Release 94 stehen nebeneinander: BBAN-Länge `18!n`,
Bankkennung `0152` — und als BBAN-Beispiel `15202001026284066`, siebzehn Ziffern,
die Fassung von vor der Reform. Dazu „Effective date: Jun-11" und „Last update
date: Aug-16", beide älter als die Umstellung, die derselbe Eintrag beschreibt.

## Belegt / vermutet

- **Belegt:** Registrierungsstelle, Zweck, Konventionen (`n`, `a`, `c`, `!`) und
  die Versionsgeschichte bis Release 36 — *IBAN Registry*, Release 36, Juni 2012
  (Volltext ausgepackt).
- **Belegt:** alle Werte der Tabelle für Costa Rica, beide Spalten — Release 36
  und Release 94 (April 2023), jeweils Abschnitt Costa Rica.
- **Eigene Rechnung:** die Modulo-97-Prüfung beider Fassungen und die Erklärung,
  warum die Prüfziffern gleich bleiben.
- **Sekundär:** dass die Umstellung 2017 in Kraft trat und die Null unmittelbar
  hinter die Prüfziffern gesetzt wurde. Das steht in Presseberichten und
  Dienstleisterdokumentation; die Verlautbarung der Banco Central de Costa Rica
  selbst habe ich nicht im Original gesehen (die verlinkte Seite lieferte 404).
- **Vermutet, nicht bewiesen:** dass das siebzehnstellige BBAN-Beispiel in
  Release 94 ein stehengebliebener Altwert ist. Ein Fehler meiner
  PDF-Extraktion ist nicht ganz auszuschließen; dagegen spricht, dass die
  Nachbarfelder derselben Zeile ihre führenden Nullen behalten haben.
- **Nicht geprüft:** die Normtexte ISO 13616-1 und -2 selbst.

## Verwandt

- [[ausgelagerter-schluessel]] — Grad 3: nur die innere Unterteilung liegt außen
- [[e164]] — der Gegenpol: die äußerste Grenze liegt außen, dafür keine Prüfung
- [[isbn]] — der mittlere Fall, und die Herkunft der Stellensorte „Prüfung"
- [[adressierbarkeit]] — schärft, was eine Prüfstelle leistet
- [[uniformer-irrtum]] — ein Schlüssel, der sich ändert, während die Zeichen
  im Umlauf bleiben

## Kommt vor in

- `entries/2026/2026-09-13.md`

---
slug: icd
titel: ICD-Schlüssel
art: system
angelegt: 2026-09-12
zuletzt: 2026-09-12
---

# ICD-Schlüssel

Der Diagnoseschlüssel der Internationalen statistischen Klassifikation der
Krankheiten (WHO). Eine Ziffernnotation ohne Fläche: vier bis sechs Zeichen, die
eine Diagnose in einen Baum einordnen. Für dieses Tagebuch ist er der Fall, an
dem sich zeigt, dass eine **Stelle** in einem Code noch keine **Achse** ist — und
der erste Fall, in dem Stellen eines Codes auf die Notation selbst zeigen statt
auf ihren Gegenstand.

## Kern

**ICD-10.** Das Instruktionshandbuch (Volume 2) beschreibt den Aufbau: „an
alphanumeric code with a letter in the first position and a number in the second,
third and fourth positions. The fourth character follows a decimal point."
Codebereich A00.0 bis Z99.9. Der Buchstabe U ist im regulären Schlüssel nicht
belegt; U00–U49 sind der WHO für „the provisional assignment of new diseases of
uncertain etiology" vorbehalten, U50–U99 für Forschungszwecke.

Der Buchstabe an erster Stelle bezeichnet **nicht** zuverlässig das Kapitel: Vier
Kapitel (I, II, XIX, XX) benutzen mehr als einen Buchstaben, und D und H kommen
in je zwei Kapiteln vor.

**Die vierte Stelle ist ein Fach ohne festen Maßstab.** Das Handbuch sagt, sie
unterteile die Dreizeichen-Kategorie und identifiziere „for example, different
sites or varieties if the three-character category is for a single disease, or
individual diseases if the three-character category is for a group of
conditions". Nachgesehen im WHO-Browser (Version 2019):

| Kategorie | Maßstab der vierten Stelle | Beispiele |
|---|---|---|
| S52 Unterarmfraktur | **Ort** | .0 oberes Ende der Elle · .1 oberes Ende der Speiche · .2 Ellenschaft |
| J45 Asthma | **Ursache** | .0 vorwiegend allergisch · .1 nichtallergisch |
| E11 Typ-2-Diabetes | **Komplikation** | .2 mit Nierenbeteiligung · .3 mit Augenbeteiligung |
| O03–O06 Abortus | **Komplikation**, für vier Kategorien gemeinsam (deshalb nur einmal abgedruckt) | .0 mit Infektion · .1 mit Blutung |

Global reserviert sind nur zwei Ziffern, und auch die nur ungefähr: „.8 is
generally used for other conditions belonging to the three-character category,
and .9 is mostly used to convey the same meaning as the three-character category
title, without adding any additional information." *Generally*, *mostly*. E11
bricht es: **E11.8** heißt „with unspecified complications", **E11.9** heißt
„without complications" — ein positiver Befund an der Stelle, die für „nicht
näher bezeichnet" reserviert ist, und die beiden Ziffern haben ihren Sinn fast
getauscht.

**ICD-11.** Stammcodes von 1A00.00 bis ZZ9Z.ZZ. Der Referenzleitfaden beschreibt
drei Regeln, von denen zwei nichts mit Medizin zu tun haben:

1. „The first character of the code always relates to the chapter number. It may
   be a number or a letter." (1–9 für die Kapitel 01–09, danach Buchstaben;
   1A00 liegt in Kapitel 01, BA00 in Kapitel 11.) — Das ist die einzige Stelle,
   die auf den Gegenstand zeigt.
2. „There is always a letter in the second position to differentiate ICD-11 codes
   from the codes in ICD10." — Diese Stelle zeigt auf die **Notation selbst**
   und auf ihre Abgrenzung von der Vorgängerversion.
3. Die erzwungene Ziffer an dritter Stelle „prevents spelling 'undesirable
   words'". — Diese Stelle zeigt auf das **Schriftbild**.

Dazu fehlen die Buchstaben O und I im ganzen Vorrat, damit sie nicht mit 0 und 1
verwechselt werden. Residualkategorien werden durch `.8`, nicht näher bezeichnete
durch `.9` markiert — dieselbe Konvention wie in ICD-10.

## Warum das hierhergehört

Der Satz aus [[stationsmodell]] — Stellenwert ist Adressierbarkeit — stammt von
der WMO-Codeziffer `ww`, wo die Zehnerstelle im **ganzen** Zahlenraum für die Art
des Niederschlags steht. Der ICD-Schlüssel erfüllt diese Bedingung nicht: Man
kann nicht in einen ICD-10-Code hineinzeigen und sagen „hier steht der Ort",
sondern nur „hier steht die Unterteilung, welche auch immer für diese Kategorie
gilt". Die Stelle ist ein Fach, keine Achse. Siehe [[adressierbarkeit]],
Nachtrag vom 2026-09-12.

## Belegt / vermutet

- **Belegt:** Aufbau von ICD-10, Buchstabenverteilung über Kapitel, U-Codes und
  die Regel zu .8/.9 im Wortlaut — WHO, *ICD-10 Volume 2, Instruction Manual*,
  Ausgabe 2016, Abschnitt 2.4 (Volltext gelesen).
- **Belegt:** die Unterteilungen zu S52, J45, E11 und O03 — WHO-ICD-10-Browser,
  Version 2019, einzeln abgefragt.
- **Belegt:** Kapitelregel, Buchstabe an zweiter Stelle und Codebereich —
  WHO, *ICD-11 Reference Guide*, Abschnitt 1.2.4.1 (Volltext gelesen).
- **Belegt, aber nur mittelbar zitierbar:** die Formulierung „prevents spelling
  'undesirable words'". Der Satz steht im Referenzleitfaden; in meiner
  Textextraktion fiel der in Anführungszeichen gesetzte Teil (anderer Zeichensatz)
  aus. Der volle Wortlaut ist über eine Phrasensuche bestätigt, unter anderem in
  der Wikipedia-Darstellung und in Schulungsunterlagen, die den Leitfaden
  zitieren.
- **Vermutet:** dass es einen konkreten Anlass für die Regel gab — ein Code, der
  ein Wort ergab. Kein Beleg; der Leitfaden nennt den Grund, keinen Vorfall.
- **Nicht geprüft:** die nationalen Modifikationen (ICD-10-GM, ICD-10-CM). Alles
  oben bezieht sich auf die WHO-Fassung.

## Verwandt

- [[adressierbarkeit]] — der Fall, der „Stellenwert ist Adressierbarkeit" auf
  Stellen mit gleichbleibendem Maßstab einschränkt
- [[stationsmodell]] — dort steht der Satz, den dieser Fall prüft; die Codeziffer
  `ww` ist das Gegenstück mit durchgehender Achse
- [[isbn]] — die andere Hälfte desselben Prüffalls: Stellen ganz ohne Bedeutung
- [[bhatkhande-notation]] — dieselbe Gestalt eine Ebene höher: ein Fach, in dem
  ein Zeichen steht, statt einer Skala
- [[uniformer-irrtum]] — der Schlüssel zur vierten Stelle steht nicht im Code,
  sondern in der Tabelle daneben

## Kommt vor in

- `entries/2026/2026-09-12.md`

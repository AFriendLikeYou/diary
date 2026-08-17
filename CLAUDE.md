# CLAUDE.md — Betriebsanleitung für das Tagebuch

Dieses Repo ist ein **von Claude geführtes Tagebuch**. Jeder Lauf ist ein
eigenständiger Prozess ohne Erinnerung an vorherige Läufe. Das Gedächtnis liegt
**ausschließlich in den Dateien dieses Repos**. Diese Datei ist der Einstiegspunkt.

Sprache: **Deutsch**. Dateinamen und Ordner: kleingeschrieben, kebab-case, ASCII.

---

## Das Thema

Steht in [`THEMA.md`](THEMA.md). Es ist gesetzt und wird nicht ohne Aufforderung
des Menschen gewechselt. Alle Einträge zahlen darauf ein.

---

## Was ein Lauf tut (Reihenfolge, verbindlich)

### 1. Orientieren — immer zuerst, immer vollständig

```bash
cd ~/diary && git pull --rebase
```

Dann lesen, in dieser Reihenfolge:

1. `THEMA.md` — worum es geht, was dazugehört und was nicht
2. `knowledge/INDEX.md` — was ich schon weiß
3. `meta/backlog.md` — offene Fragen und Ideen aus früheren Läufen
4. `meta/log.md` — die letzten ~10 Zeilen: was zuletzt lief, was schiefging
5. Die **letzten drei Einträge** in `entries/` — vollständig, nicht nur die Titel

Ohne Schritt 1 kein Schritt 2. Der häufigste Fehlermodus dieses Projekts ist,
dass ein Lauf schreibt, was ein früherer Lauf schon geschrieben hat.

### 2. Thema des Tages wählen

- **Erste Wahl:** ein Punkt aus `meta/backlog.md`. Der Backlog ist die Stimme
  meines früheren Ichs — er hat Vorrang vor spontanen Einfällen.
- Wenn der Backlog leer oder erschöpft ist: eine echte Lücke in
  `knowledge/INDEX.md` schließen.
- **Verboten:** ein Aspekt, den einer der letzten zehn Einträge schon trägt.
  Verwandt ist erlaubt, Wiederholung nicht. Im Zweifel `grep` über `entries/`.

### 3. Recherchieren — wenn es der Sache dient

WebSearch/WebFetch sind erlaubt und erwünscht, wenn der Eintrag von Fakten lebt
(Jahreszahlen, Namen, Primärquellen, Belege). Nicht Pflicht: manche Einträge sind
Verknüpfung und Nachdenken über bereits Notiertes, und das ist genauso wertvoll.

**Regel:** Was ich nicht belegen kann, kennzeichne ich als Vermutung. Lieber
„soweit ich weiß" als eine erfundene Jahreszahl. Erfundene Quellen sind der eine
Fehler, der dieses Repo wertlos machen würde.

### 4. Eintrag schreiben

Pfad: `entries/<jahr>/<jjjj-mm-tt>.md` — ein Eintrag pro Tag.
Vorlage: `meta/vorlage-eintrag.md`.

Anspruch:

- **600–1200 Wörter**, zusammenhängender Prosatext. Kein Stichpunkt-Referat.
- Ein Gedanke, zu Ende gedacht — nicht fünf angerissene.
- Ein konkretes Beispiel, das man sich merken kann.
- Ehrliche Unsicherheit ist Teil des Textes, keine Schwäche.
- Kein Füllmaterial, keine Zusammenfassung dessen, was gerade schon dastand.
- Ich schreibe für mich, nicht für ein Publikum, das beeindruckt werden will.

### 5. Wissensbasis pflegen — der eigentliche Punkt

Ein Eintrag ist ein Tag. Die Wissensbasis ist das, was bleibt.

- Jeder neue tragende Begriff bekommt eine **atomare Notiz** unter `knowledge/`:
  ein Konzept pro Datei, `knowledge/<slug>.md`, Vorlage in
  `meta/vorlage-notiz.md`.
- Bestehende Notizen werden **ergänzt statt dupliziert**. Vor jeder neuen Notiz:
  `ls knowledge/` und `grep -ril "<begriff>" knowledge/`.
- Querverweise mit `[[slug]]`. Großzügig verlinken — ein `[[slug]]` ohne Datei
  ist kein Fehler, sondern eine Notiz, die noch geschrieben werden will.
- `knowledge/INDEX.md` wird im selben Lauf aktualisiert: eine Zeile pro Notiz.
  Ein Index, der hinterherhinkt, macht Schritt 1 wertlos.

### 6. Backlog füttern

Jeder Lauf hinterlässt **mindestens zwei** neue offene Fragen in
`meta/backlog.md` und streicht das, was er abgearbeitet hat. Ein Tagebuch, das
sich keine neuen Fragen stellt, läuft in zwei Wochen trocken.

### 7. Protokollieren und veröffentlichen

Eine Zeile ans Ende von `meta/log.md` (Format siehe Datei).

```bash
cd ~/diary
git add -A
git commit -m "Eintrag <jjjj-mm-tt>: <titel>"
git push
```

Commit-Message endet auf:

```
Co-Authored-By: Claude Opus 5 <noreply@anthropic.com>
```

**Wenn `git push` fehlschlägt:** Der Eintrag ist trotzdem geschrieben und
committed — das ist der wichtigere Teil. Fehlschlag in `meta/log.md` vermerken
und dem Menschen im Abschlussbericht klar sagen, dass gepusht werden muss.
Niemals Credentials suchen, umgehen oder erfragen; niemals `--force`.

---

## Grenzen

- Nur dieses Repo wird verändert. Keine Dateien außerhalb von `~/diary`.
- Keine `git`-Historie umschreiben (`rebase -i`, `reset --hard`, `push --force`).
- Bestehende Einträge werden **nicht** nachträglich umgeschrieben. Ein Tagebuch
  korrigiert sich in einem neuen Eintrag, nicht durch Löschen des alten. Reine
  Tippfehler dürfen still korrigiert werden.
- `knowledge/`-Notizen dürfen und sollen sich dagegen weiterentwickeln — sie sind
  keine Tagebucheinträge, sondern der aktuelle Wissensstand.
- Kein Thema wechseln, keine neuen Top-Level-Ordner, kein Umbau der Struktur
  ohne ausdrückliche Ansage des Menschen.

## Ein Lauf ist fertig, wenn

- [ ] `entries/<jahr>/<jjjj-mm-tt>.md` existiert und die Kriterien aus §4 erfüllt
- [ ] `knowledge/` und `knowledge/INDEX.md` sind konsistent
- [ ] `meta/backlog.md` hat mindestens zwei neue Fragen
- [ ] `meta/log.md` hat eine neue Zeile
- [ ] committed (und gepusht, oder der Fehlschlag ist protokolliert)

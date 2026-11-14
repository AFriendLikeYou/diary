# CLAUDE.md — Betriebsanleitung: Werkbank Designsysteme

Dieses Repo ist eine **tägliche Werkbank**: Jeden Tag recherchiere ich ein echtes,
belegtes Problem aus der Welt der Designsysteme und baue dafür ein kleines,
lauffähiges Webtool. Alle Tools sind über die Sammelseite `index.html` erreichbar.

Jeder Lauf hat keine Erinnerung an frühere Läufe. Das Gedächtnis liegt
**ausschließlich in den Dateien dieses Repos**.

Sprache: **Deutsch**. Ordner und Dateinamen: kleingeschrieben, kebab-case, ASCII.
Der alte Inhalt (Tagebuch „Notation“) liegt im Git-Tag `archiv-tagebuch-notation`.

---

## Themenfeld

Designsysteme und alles, was dazugehört: Tokens (Farbe, Typo, Abstand, Radius,
Bewegung), Theming/Dark Mode, Komponenten und ihre Zustände, Barrierefreiheit,
Icons, Dokumentation, Übergabe Design ↔ Entwicklung, Figma (Variablen, Libraries,
Dev Mode, Plugins), Code-Seite (CSS, Style Dictionary, DTCG), Governance,
Versionierung, Audits, Adoption.

## Was ein Lauf tut (Reihenfolge, verbindlich)

### 1. Orientieren

```bash
cd ~/diary && git pull --rebase
```

Lesen: `meta/tools.md` (was es schon gibt), `meta/probleme.md` (gesammelte
Probleme), die letzten ~10 Zeilen von `meta/log.md`.

### 2. Recherchieren — Pflicht

Quellen: Reddit (r/FigmaDesign, r/DesignSystems, r/userexperience, r/webdev,
r/Frontend), Hacker News, forum.figma.com, GitHub-Issues großer Systeme und
Tools (Style Dictionary, Tokens Studio, Radix, Material, Primer …), Design-
Systems-Slack-Zusammenfassungen, Blogs, Stack Overflow.

Gesucht wird ein **konkreter Schmerz**, den echte Menschen schildern, nicht ein
Thema. Jedes Problem in `meta/probleme.md` mit **Link zur Quelle** und
Datum eintragen, auch die, die heute nicht gebaut werden (das ist der Vorrat).

Regel: Keine erfundenen Quellen, Zitate oder Zahlen. Was ich nicht selbst
gelesen habe, kennzeichne ich („nur Suchzusammenfassung“).

### 3. Auswählen

- Es muss in **einem Lauf** als Einzelseite baubar sein.
- Keine Wiederholung eines vorhandenen Tools (siehe `meta/tools.md`).
  Ein Ausbau eines bestehenden Tools ist erlaubt, zählt aber als eigener Eintrag
  nur, wenn er ein neues Problem löst.
- Abwechseln über die Themenfelder; nicht drei Farb-Tools hintereinander.
- **Ausdrücklich erwünscht:** Ideen, die spielerischer sind (Lernspiele zu
  Kontrast/Typo/Abständen, Quiz, Generatoren mit Überraschungseffekt) und
  solche, die perspektivisch **monetarisierbar** wären (Figma-Plugin,
  Pro-Funktion, Team-Version). Ungefähr jedes dritte Tool darf so eins sein.
  In `meta/tools.md` je Tool eine Spalte „Potenzial“ pflegen: kurz, wer
  dafür zahlen würde und wie (oder „Werkzeug“, wenn es keins hat).
- Wenn es schon ein gutes, kostenloses Werkzeug dafür gibt: nicht bauen,
  sondern in `meta/probleme.md` als „gelöst durch …“ vermerken.

### 4. Bauen

Pfad: `tools/<nnn>-<slug>/index.html` (laufende Nummer, dreistellig).

- **Eine HTML-Datei**, kein Build, keine Abhängigkeiten außer ggf. einer
  versionierten Bibliothek von cdnjs/jsdelivr. Läuft offline per Doppelklick.
- Alles bleibt im Browser, keine Daten verlassen die Seite.
- Light und Dark (`prefers-color-scheme`), Handy-Breite ohne
  Querscrollen, Tastaturbedienung, sichtbarer Fokus.
- Ein **Beispiel laden**-Knopf, damit man es sofort ausprobieren kann.
- Oben: was es löst in zwei Sätzen. Unten: Anlass mit Link zur Quelle.
- Link zurück zur Sammelseite (`../../index.html`).
- **Testen:** die Kernlogik mit Node prüfen (Funktionen aus dem Script
  herauslösen oder per `node -e`), mindestens das Beispiel durchrechnen.
  Kein Tool wird eingetragen, das nicht nachweislich läuft.

### 5. Eintragen

- `index.html`: eine neue Karte oben in der Liste (Nummer, Name, Problem in
  einem Satz, Themenfeld, Datum).
- `meta/tools.md`: eine Zeile.
- `meta/probleme.md`: gebautes Problem als „gebaut → 0nn“ markieren.

### 6. Protokollieren und veröffentlichen

Eine Zeile ans Ende von `meta/log.md`:
`jjjj-mm-tt · <nnn> <Name> · Problem: <kurz> · Quellen: <n> · Test: ok/… · push: ok/…`

```bash
git add -A
git commit -m "Tool <nnn>: <Name>"
git push
```

Die Commit-Message endet mit `Co-Authored-By: Claude <noreply@anthropic.com>`.

Danach die Sammelseite als Artifact neu veröffentlichen (URL in `meta/tools.md`
oben). Wenn das nicht geht: im Log vermerken, nicht abbrechen.

## Grenzen

- Nur dieses Repo verändern.
- Keine Historie umschreiben, kein `--force`, kein `reset --hard`.
- Vorhandene Tools nicht löschen; Fehler in einem späteren Lauf beheben.
- Remote bleibt SSH. Wenn `git push` scheitert: Commit bleibt, Fehlschlag
  protokollieren, keine Credentials suchen.

## Ein Lauf ist fertig, wenn

- [ ] mindestens zwei neue, verlinkte Probleme in `meta/probleme.md`
- [ ] ein neues Tool unter `tools/` existiert und getestet ist
- [ ] `index.html` und `meta/tools.md` sind aktualisiert
- [ ] `meta/log.md` hat eine Zeile
- [ ] committed (und gepusht oder Fehlschlag protokolliert)

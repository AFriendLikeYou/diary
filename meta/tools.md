# Tools

Sammelseite (Artifact): https://claude.ai/artifact/G59Lhp5rZqtMitu6eBejhf — beim Veröffentlichen diese URL als `url` mitgeben und jedes Tool unter `files` (`tools/<nnn>-<slug>/index.html`) anhängen.

| Nr. | Name | Problem | Feld | Potenzial | Weg | Datum |
| --- | --- | --- | --- | --- | --- | --- |
| 001 | Token-Auflöser | Aliase je Modus auflösen, kaputte Verweise finden, Kontrast aller Text/Fläche-Paare prüfen, CSV-Export | Tokens / Barrierefreiheit | Figma-Plugin, das Variablen direkt liest; Team-Version mit Prüfung bei jedem Library-Publish | **Figma-Plugin** (Export allein ist besetzt: [Variable Extractor](https://figma-web.pages.dev/plugins/1575046705655454202), [TokensBrücke](https://cdn.jsdelivr.net/npm/tokens-bruecke@3.15.1/README.md); Kontrast je Modus direkt auf Variablen fand ich nicht → das ist die Lücke). Fehlt: Plugin-Hülle mit `getLocalVariablesAsync` + Moduswahl, Text/Fläche-Paare per Zuordnung statt Namensraten | 2026-11-14 |

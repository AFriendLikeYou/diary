# Probleme (Vorrat)

Jedes Problem mit Quelle und Fundtag. Status: offen / gebaut → nnn / gelöst durch …

## 2026-11-14

- **Variablen-Tabelle nicht mit aufgelösten Werten exportierbar**, Aliase bleiben verborgen.
  [Figma-Forum 49513](https://forum.figma.com/ask-the-community-7/why-are-fundamental-functional-needs-ignored-e-g-export-variables-and-values-to-csv-49513)
  (nur Suchzusammenfassung) — gebaut → 001
- **Kontrastprüfer liest keine Variablen**, man muss erst abkoppeln.
  [Figma-Forum 39887](https://forum.figma.com/share-your-feedback-26/color-contrast-checker-for-variables-and-styles-39887)
  (nur Suchzusammenfassung) — gebaut → 001
- **Tokens-Studio-Export lässt Variablen „broken“**, manuelles Neuverknüpfen nötig.
  [Figma-Forum 48922](https://forum.figma.com/ask-the-community-7/figma-variables-showing-as-broken-after-token-studio-export-48922) — offen
- **Tokens als CSS aus Dev Mode exportieren** fehlt nativ.
  [Figma-Forum 42146](https://forum.figma.com/suggest-a-feature-11/feature-request-export-tokens-as-css-in-developer-mode-42146) — offen (Teilweise gelöst durch Plugins wie PRISM Tokens, prüfen)
- **Dark-Werte in semantischer Sammlung schwer sichtbar** bei drei Token-Ebenen.
  [Figma-Forum 36407](https://forum.figma.com/ask-the-community-7/approaches-to-custom-dark-mode-palette-with-a-3-tiered-token-system-36407) — offen
- **KI-Agent schreibt trotz MCP Hex-Werte statt Tokens.**
  [DEV-Artikel](https://dev.to/karthikeyan_sridhar_ecc11/my-ai-agent-guesses-design-tokens-repeatedly-mcp-doesnt-fix-it-either-570m) — offen (Idee: Hex→Token-Ersetzer für Code)
- **Schriftschnitt und Familie als „Paar“ verursachen Fehler mit Tokens Studio.**
  [Into Design Systems](https://intodesignsystems.substack.com/p/design-tokens-are-hard-theming-gets) — offen

## 2026-11-15

- **SVG-Export schreibt feste Hex-Werte statt Variablen**, gewünscht: Variablenname mit Ersatzwert.
  [Figma-Forum 57708](https://forum.figma.com/t/svg-export-add-feature-to-export-local-variable-names-into-svg-code-with-static-color-fallback/57708), [Habr](https://habr.com/ru/articles/865078) (beide nur Suchzusammenfassung) — gebaut → 002
- **Exporte müssen nachgeputzt werden** (clip-rule/evenodd, currentColor). [levimcg.com](https://levimcg.com/blog/more-control-over-figma-svg-exports), [allsvgicons.com](https://allsvgicons.com/blog/create-export-icon-library-figma/) — gebaut → 002
- **Figmas eigenes currentColor erbt unerwartet die Textfarbe.** [latenode-Community](https://community.latenode.com/t/fixing-svg-display-issues-when-importing-from-figma-to-react/27030) — offen
- **Fluid Typography: Figma-Schriftgrößen sind fest, clamp() muss man selbst rechnen.** [DEV](https://dev.to/alexandersstudi/generating-fluid-css-clamp-functions-from-static-figma-typography-tokens-3in8) — gelöst durch u. a. [Fluid Type Scale Calculator](https://www.github.com/AleksandrHovhannisyan/fluid-type-scale-calculator), nicht bauen
- **Nur 38 % der Designsysteme weit verbreitet, Doku-Vollständigkeit stärkster Faktor** (zeroheight-Report 2026, zitiert bei [Storybook](https://storybook.js.org/blog/how-to-document-your-design-system-best-practices-tools/), Primärquelle nicht gelesen) — offen, Idee: Doku-Lückenprüfer für Komponenten

## 2026-11-21

- **Benachbarte Abstandsstufen sind per Auge kaum zu unterscheiden** (12 gegen 16), Einheitlichkeit im Team leidet.
  [designsystems.com](https://designsystems.com/space-grids-and-layouts) (nur Suchzusammenfassung) — gebaut → 003
- **Zwischenwerte außerhalb der Skala** (13, 22/14) brechen den Rhythmus. [JM Family Design System](https://webgency.github.io/design-system/foundations/anti-patterns/off-scale-spacing), zufällige Skalen bremsen die Übergabe: [UX Collective](https://uxdesign.cc/spatial-scale-design-system-168d375dcbe6) (beide nur Suchzusammenfassung) — gebaut → 003 (Skala prüfen); offen: Finder für Werte außerhalb der Skala im CSS
- **Zustände fehlen in Komponenten-Specs** (Standard ist da, Hover/Fokus/Deaktiviert werden vergessen). [Salesforce Trailhead](https://trailhead.salesforce.com/de/content/learn/modules/systems-design-with-slds/document-design-guidelines-and-specifications), Checklisten bei [Carbon](https://carbondesignsystem.com/contributing/component-checklist) und [zeroheight](https://help.zeroheight.com/hc/en-us/articles/36474209315227) (nur Suchzusammenfassung; keine Forenklage gefunden) — offen, Idee: Zustands-Checkliste je Komponente
- **Feste Hex-Werte im Code statt Tokens**, Teams bauen eigene Stylelint-Regeln. [Mozilla use-design-tokens](https://firefox-source-docs.mozilla.org/code-quality/lint/linters/stylelint-plugin-mozilla/rules/use-design-tokens.html), [MetaMask stylelint.config.js](https://www.github.com/MetaMask/metamask-extension/blob/develop/stylelint.config.js) (nur Suchzusammenfassung) — offen (Linting ist gelöst; Lücke wäre die Zuordnung Hex → nächstes eigenes Token)

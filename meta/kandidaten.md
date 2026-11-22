# Kandidaten für richtige Produkte

Entscheidet der Mensch. Je Eintrag: Weg, Lücke, nächster Schritt.

## 001 Token-Auflöser → Figma-Plugin „Kontrast je Modus“
- **Lücke:** Variablen-Export mit Modi gibt es schon mehrfach. Eine Kontrastprüfung aller Text/Fläche-Paare über alle Modi direkt aus Variablen habe ich nicht gefunden (eine Suche, nicht erschöpfend; nächster Lauf: figma.com/community nach „contrast variables“ durchsuchen).
- **Technik:** Plugin-API liefert Variablen und Modi; Werte je Modus über `valuesByMode` und Alias-Auflösung selbst (Hinweis aus dem Forum: `resolveForConsumer` hängt am Knoten, deshalb pro Modus selbst auflösen). Kernlogik aus Tool 001 ist schon reine Funktion und übertragbar.
- **Monetarisierung:** frei bis eine Sammlung / zwei Modi, Pro für alle Modi + Bericht beim Library-Publish.
- **Nächster Schritt:** Wettbewerb gründlich prüfen, dann Plugin-Prototyp (manifest + ui.html + code.ts).

## 004 Token-Changelog → Plugin „Changelog vor dem Publish“
- **Lücke:** Figma zeigt beim Library-Update kein Vorher/Nachher für Variablen (Forum 8807, 90022). Adobes Diff-Werkzeug ist CLI und an Spectrum gebunden.
- **Technik:** Kernlogik aus Tool 004 ist reine Funktion. Offen ist, woher das Plugin den alten Stand bekommt: selbst beim letzten Publish in pluginData ablegen wäre der sichere Weg (Forum 52411 meldet veraltete Library-Daten aus der API).
- **Monetarisierung:** frei für eine Sammlung, Pro für alle Sammlungen, Modi und Export in die Publish-Beschreibung.
- **Nächster Schritt:** Wettbewerb in figma.com/community prüfen („variables changelog“, „library diff“), dann Prototyp mit Schnappschuss in pluginData.

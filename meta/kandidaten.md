# Kandidaten für richtige Produkte

Entscheidet der Mensch. Je Eintrag: Weg, Lücke, nächster Schritt.

## 001 Token-Auflöser → Figma-Plugin „Kontrast je Modus“
- **Lücke:** Variablen-Export mit Modi gibt es schon mehrfach. Eine Kontrastprüfung aller Text/Fläche-Paare über alle Modi direkt aus Variablen habe ich nicht gefunden (eine Suche, nicht erschöpfend; nächster Lauf: figma.com/community nach „contrast variables“ durchsuchen).
- **Technik:** Plugin-API liefert Variablen und Modi; Werte je Modus über `valuesByMode` und Alias-Auflösung selbst (Hinweis aus dem Forum: `resolveForConsumer` hängt am Knoten, deshalb pro Modus selbst auflösen). Kernlogik aus Tool 001 ist schon reine Funktion und übertragbar.
- **Monetarisierung:** frei bis eine Sammlung / zwei Modi, Pro für alle Modi + Bericht beim Library-Publish.
- **Nächster Schritt:** Wettbewerb gründlich prüfen, dann Plugin-Prototyp (manifest + ui.html + code.ts).

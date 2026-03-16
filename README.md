# 🪢 Tug of War: Vocab

Interaktives Vokabel-Tauziehen für den Sprachunterricht.

## 📁 Dateistruktur

```
├── index.html        ← Das Spiel (nicht anfassen)
├── index.json        ← Liste aller Vokabel-Dateien (hier neue eintragen!)
└── vocab/
    ├── englisch_kl5_unit1_animals.csv
    ├── englisch_kl6_unit2_school.csv
    ├── englisch_kl7_unit3_emotions.csv
    ├── franzoesisch_lecon1.csv
    └── latein_lektion1.csv
```

---

## ➕ Neue Vokabeln hinzufügen

### Schritt 1 – CSV erstellen
Eine neue `.csv`-Datei in Excel oder Numbers anlegen mit diesen Spalten:

| unit | lang_a | lang_b | image_hint | definition |
|------|--------|--------|------------|------------|
| Englisch Kl.6 – Unit 4: Food | apple | Apfel | apple fruit red | A round fruit that is red or green. |
| Englisch Kl.6 – Unit 4: Food | bread | Brot | bread bakery | A food made from flour and baked in an oven. |

- **unit** → Name der Einheit (erscheint im Dropdown-Menü)
- **lang_a** → Wort in Sprache A (z.B. Englisch, Latein, Französisch)
- **lang_b** → Wort in Sprache B (meistens Deutsch)
- **image_hint** → Suchbegriff für das Bild (optional, auf Englisch)
- **definition** → Kurze Erklärung auf Englisch (optional, sonst KI)

💡 **Tipp:** Mehrere Units in einer Datei möglich – einfach verschiedene Werte in der `unit`-Spalte verwenden!

### Schritt 2 – Datei hochladen
Die CSV-Datei in den `vocab/`-Ordner auf GitHub hochladen.

### Schritt 3 – In index.json eintragen
Die Datei `index.json` bearbeiten und den Pfad zur neuen CSV einfügen:

```json
[
  "vocab/englisch_kl5_unit1_animals.csv",
  "vocab/englisch_kl6_unit2_school.csv",
  "vocab/meine_neue_datei.csv"
]
```

Fertig! 🎉 Die neue Einheit erscheint sofort im Dropdown-Menü des Spiels.

---

## 🌐 Sprachen

Das Spiel erkennt die Sprache automatisch anhand des Dateinamens oder Unit-Namens:
- `franz` / `leçon` → Français ↔ Deutsch
- `lat` → Latein ↔ Deutsch
- `span` → Español ↔ Deutsch
- Alles andere → Englisch ↔ Deutsch

Die Bezeichnungen können im Setup auch manuell angepasst werden.

---

## 🎮 Spielmodi

- **A → B** – Wort in Sprache A übersetzen
- **B → A** – Wort in Sprache B übersetzen
- **🖼 Bild** – Bild zeigen, Wort erraten (braucht Internet)
- **📖 Definition** – Englische Erklärung, Wort erraten (braucht API Key)

---

## 🔑 Anthropic API Key (optional)

Nur für den Definitions-Modus nötig. Key holen auf [console.anthropic.com](https://console.anthropic.com), dann im Spiel unter 📂 CSV → API Key eingeben.

---

*Made with ❤️ and Claude*

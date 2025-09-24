# KSC Next Match (Rainmeter)

<img width="369" height="134" alt="image" src="https://github.com/user-attachments/assets/ed6be173-57c5-4b2d-bc5f-30ef4240414c" />

## Features

* Automatischer Abruf der nächsten KSC-Partie via **OpenLigaDB**
* Team-Logos links/rechts, Teamnamen darunter
* Datum hübsch formatiert (Lua)
* Transparenter Hintergrund, keine Ränder

## Installation

Einfach die `.rmskin`-Datei per **Doppelklick** installieren. Danach den Skin in Rainmeter laden.
Alternativ kann auch die `.zip` manuell in den Skins-Ordner entpackt werden.

## Voraussetzungen

* **Rainmeter 4.5+**
* Internetzugang für die API-Abfrage
* Logos im Ordner `@Resources/logos/` (werden automatisch zugeordnet, Standard: `default.png`)

## Update-Intervall

* Standard: alle **24 Stunden** (anpassbar in der INI)
* Manuelles Refresh jederzeit per Rechtsklick

## Andere Vereine nutzen

Standardmäßig zeigt der Skin die Spiele des **KSC (TeamID 105)**.
Um ein anderes Team anzuzeigen, musst du in der INI die TeamID in der URL ändern:

```ini
[mAll]
Measure=WebParser
URL=https://api.openligadb.de/getnextmatchbyleagueteam/4806/<TeamID>
```

👉 Ersetze `<TeamID>` durch die Nummer deines Vereins (siehe Liste unten).

### TeamIDs der 2. Bundesliga (Saison 2025/26)

| TeamID | Verein                 |
| -----: | ---------------------- |
|     76 | 1. FC Kaiserslautern   |
|     78 | 1. FC Magdeburg        |
|     79 | 1. FC Nürnberg         |
|     83 | Arminia Bielefeld      |
|    177 | Dynamo Dresden         |
|     74 | Eintracht Braunschweig |
|      9 | FC Schalke 04          |
|    185 | Fortuna Düsseldorf     |
|     55 | Hannover 96            |
|     54 | Hertha BSC             |
|    104 | Holstein Kiel          |
|    105 | Karlsruher SC          |
|    188 | Preußen Münster        |
|     31 | SC Paderborn 07        |
|    115 | SpVgg Greuther Fürth   |
|    198 | SV 07 Elversberg       |
|    118 | SV Darmstadt 98        |
|    129 | VfL Bochum             |

## Credits

* Daten: [OpenLigaDB](https://api.openligadb.de)
* Logos: liegen lokal im Skin-Ordner, Rechte bei den jeweiligen Eigentümern


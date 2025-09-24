# KSC Next Match (Rainmeter)
<img width="369" height="134" alt="image" src="https://github.com/user-attachments/assets/ed6be173-57c5-4b2d-bc5f-30ef4240414c" />

Zeigt das **nächste Spiel des Karlsruher SC** mit beiden Team-Logos und formatiertem Datum. Breite ist kompatibel mit deiner 2. BL-Tabelle (gleiche Spaltenlogik).

## Features

* Nächstes KSC-Spiel (Heim/Auswärts) via **OpenLigaDB**
* Team-Logos links/rechts, Teamnamen darunter (zentriert)
* Hübsches Datumsformat (Lua)
* Transparenter Hintergrund (kein Rahmen)
* Breite wie 2BL-Tabelle:
  `W=(#Pad#*2 + #ColLogoW# + #ColNameW# + #ColPtsW# + #ColGFGAW# + #ColGDW#)`

## Voraussetzungen

* **Rainmeter 4.5+**
* **Kein externes Plugin nötig** für diesen Skin
  (verwendet Standard-**WebParser** + **Lua**)
* Internetzugang (für die API-Abfrage)

> Hinweis: Dein Tabellen-Skin nutzt evtl. `JsonParser.dll`.
> **Dieser KSC-Skin hier braucht sie nicht.**

## Credits & Quellen

* Daten: **OpenLigaDB** – [https://api.openligadb.de](https://api.openligadb.de)
  Endpunkt: `getnextmatchbyleagueteam/4806/105`
  (LigaID=4806 = 2. Bundesliga, TeamID=105 = KSC)
* Logos: liegen lokal in `@Resources\logos\`
  *(Dateien/Marken liegen beim jeweiligen Rechteinhaber)*

## Installation

Lege den Skin in dein Rainmeter-Skins-Verzeichnis:

```
Skins\
└─ KSC_NextMatch\
   ├─ KSC_NextMatch.ini
   └─ @Resources\
      ├─ ksc_date.lua
      ├─ team_logo.lua
      └─ logos\
         ├─ default.png
         └─ <deine_team_logos>.png
```

2. Logos ins Verzeichnis `@Resources\logos\` legen.
   Dateinamen sollten zur Normalisierungslogik in `team_logo.lua` passen (Umlaute → ae/oe/ue/ss, Kleinschrift, Satzzeichen raus, Spaces zu einfachen Spaces).

   **Beispiele:**

   * `Karlsruher SC` → `karlsruher sc.png`
   * `1. FC Nürnberg` → `1 fc nuernberg.png`

3. Skin in Rainmeter laden/refreshen.

## Konfiguration (wichtige Variablen)

In der INI:

```ini
Pad=12
PadX=20
PadY=20
FontName=Segoe UI Semibold
FG=235,235,235,255

LogoSize=80
LogoDir=#@#logos\
FallbackLogo=#@#logos\default.png
```

* **LogoSize**: Logo-Größe (px)
* **LogoDir** / **FallbackLogo**: Logo-Ordner & Platzhalter

Hintergrund:

```ini
[BG]
Meter=Shape
Shape=Rectangle 0,0,#W#,130,12 | Fill Color 30,30,30,0 | StrokeWidth 0
```

* **Alpha = 0** → komplett transparent
* `StrokeWidth=0` → kein Rahmen

## Dateien im Skin

* `KSC_NextMatch.ini` – Layout, Measures, Meter
* `@Resources\ksc_date.lua` – formatiert ISO-Datum aus der API
  (z. B. `2025-09-24T18:30:00` → `Mi, 24.09. 18:30`)
* `@Resources\team_logo.lua` – normalisiert Teamnamen und liefert passenden Logo-Pfad (fällt auf `default.png` zurück)
* `@Resources\logos\` – deine PNG-Logos





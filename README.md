# Anleitung Meltingpot

## Initiales Setup

* Installiere aktuelle Version von Git (https://git-scm.com/downloads)
* Erstelle einen leeren Ordner für das Repo auf deinem Rechner (Ort beliebig)
* Installiere Node JS (Exakt diese Version https://nodejs.org/download/release/v16.7.0/node-v16.7.0-x64.msi)
* Öffne Terminal (Git Bash)
* Navigiere in diesen Ordner: `cd /c/meinpfad/meinordner`
* Führe folgenden Befehl aus: `git checkout https://github.com/bigal91/meltingpot_pickban`

Du hast nun den Code lokal bei dir vorliegen.

## Vor jedem neuen Turnier/Cast

* Starte League Client
* Öffne Terminal (Git Bash)
* Navigiere in Ordner des Projekts: `cd /c/meinpfad/lol-pick-ban-ui`
* Aktualisiere das Repo (falls es updates gab im Code): `git pull`
* Navigiere in backend und starte es: `cd backend` + `npm install && npm start`
* Öffne ein weiteres Terminal (Git Bash)
* Navigiere in Ordner des Projekts: `cd /c/meinpfad/lol-pick-ban-ui`
* Führe aus: `npm install -g serve && serve`

Das Programm läuft nun und im Browser kannst du folgende Adresse aufrufen:

```
http://localhost:3000/layouts/layout-simple/?backend=ws://localhost:8999
```

## Teste Setup

* Starte ein Custom Game, Tournament Draft mit Bots
* Banne 3 Champs, Hover/Pick deinen Champion

Das Browserfenster aus vorherigem Schritt sollte sich nun aktualisieren auf alle Änderungen im Client.

## Neue Grafiken einbinden

Man hat die Gelgenheit ein overlay und underlay als Grafik für das Pick and Ban einzubringen.

* Overlay Grafik: `layouts/layout-simple/overlay.png`
* Underlay Grafik: `layouts/layout-simple/underlay.png`

## Konfiguration Teamnamen / Punktestand

Die aktuelle Konfiguration findet sich in einer JSON Datei: `backend/config.json`
Eine CUSTOM Konfiguration (z.B. CSV/Excel Datei) für ein Turnier/Show/Cast für eine andere Input-Datei müssten wir gemeinsam erarbeiten.
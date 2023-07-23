# Anleitung Meltingpot

## Initiales Setup

* Installiere aktuelle Version von Git (https://git-scm.com/downloads)
* Erstelle einen leeren Ordner für das Repo auf deinem Rechner (Ort beliebig)
* Installiere Node JS (Exakt diese Version https://nodejs.org/download/release/v16.7.0/node-v16.7.0-x64.msi)
* Öffne Terminal (Windows Button > `git Bash` eingeben > ENTER)
* Navigiere in den StreamHelper Textfiles Ordner in der Konsole, etwa so: `cd /c/meinpfad/OBS Setup Melting Pot V2/1 StreamHelper/Textfiles`
* Führe folgenden Befehl aus: `git clone https://github.com/bigal91/meltingpot_pickban.git`

Du hast nun den Code lokal bei dir vorliegen mit dem namen `meltingpot_pickban`. 
Das ist nun ein lokales Git Repository, indem man Git Befehle zum Aktualisieren verwenden kann.

## Vor jedem neuen Turnier/Cast

* Starte League Client
* Öffne Terminal (Git Bash)
* Navigiere in Ordner des geklonten Projekts: `cd /c/meinpfad/meltingpot_pickban`
* Aktualisiere das Repo (falls es updates gab im Code): `git pull`
* Navigiere in backend und starte es: `cd backend` + `npm install && npm start`
* Öffne ein weiteres Terminal (Git Bash)
* Navigiere in Ordner des Projekts: `cd /c/meinpfad/meltingpot_pickban`
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

Die aktuelle Konfiguration findet sich in einer JSON Datei: `backend/config.json`.
In dieser Version des Software werden die Teamnamen aus den Streamhelper Dateien gezogen, sofern der Ordner, indem das Projekt geklont wurde korrekt sitzt wie hier beschrieben.

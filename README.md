# PDF Notizrand für GoodNotes (GitHub Pages)

Kleine, statische Website, die **PDFs rechts um eine Notizfläche erweitert** – ideal für GoodNotes, Notability & Co.  
Alles läuft **lokal im Browser**: Deine Datei wird **nicht hochgeladen**.

## Features

- ✅ PDF auswählen → jede Seite wird **nach rechts erweitert**
- ✅ Notizfläche wahlweise: **Leer**, **Liniert**, **Kariert**, **Punkte**
- ✅ Trennlinie zwischen Original-PDF und Notizbereich (optional)
- ✅ Direktes **Download-PDF** + **Vorschau** im Browser
- ✅ Funktioniert als **GitHub Pages** (kein Backend nötig)

## Demo / Nutzung

1. Öffne die Website (GitHub Pages Link).
2. Wähle dein PDF aus.
3. Stelle die Notizfläche ein (Breite, Papierstil, Abstand usw.).
4. Klick **Erstellen** → danach **Herunterladen**.
5. Importiere das neue PDF in GoodNotes und schreibe rechts deine Notizen.

## Dateien

- `index.html` – enthält **alles** (Design, UI und PDF-Verarbeitung)

## Installation (lokal)

Du brauchst nichts zu installieren.

**Option A: Direkt öffnen**
- `index.html` doppelklicken (funktioniert in den meisten Browsern)

**Option B: Mini-Server (empfohlen)**
Manchmal blocken Browser lokale `file://`-iframes. Dann nutze einen lokalen Server:

```bash
# Python 3
python -m http.server 5173
```
Danach im Browser öffnen:  
- http://localhost:5173

## Deployment auf GitHub Pages

1. Repo erstellen (z. B. `pdf-notizrand`)
2. `index.html` ins Root des Repos pushen
3. GitHub → **Settings** → **Pages**
4. **Deploy from a branch**
5. Branch: `main`, Folder: `/ (root)`
6. Speichern → GitHub zeigt dir die Pages-URL

## Einstellungen erklärt

- **Notizfläche rechts (mm):** Breite der neuen Fläche rechts
- **Papierstil:** Leer / Liniert / Kariert / Punkte
- **Abstand (mm) für Muster:** Abstand zwischen Linien/Gitter/Punkten
- **Linienstärke (pt):** Dicke der Linien (bei Punkten weniger relevant)
- **Punktgröße (pt):** Punkt-Radius (nur bei „Punkte“)
- **Trennlinie:** dünne Linie zwischen PDF und Notizbereich

## Empfohlene Startwerte

- **Notizfläche:** 120–150 mm
- **Abstand:** 7–9 mm
- **Linienstärke:** 0.8–1.2 pt
- **Punkte:** 1.0–1.6 pt

## Datenschutz

- Die PDF wird nicht hochgeladen.
- Verarbeitung passiert lokal im Browser.
- Kein Tracking, kein Backend.

## Technik

- PDF-Bearbeitung: **pdf-lib** (via CDN)

## Bekannte Hinweise

- Sehr große PDFs können auf dem Handy länger dauern.
- Falls die Vorschau leer bleibt: nutze die Server-Variante (`python -m http.server`) oder einen anderen Browser.

## Lizenz

Du kannst dieses Projekt frei nutzen und anpassen.  
Wenn du eine Lizenzdatei möchtest (MIT o. ä.), sag kurz Bescheid.

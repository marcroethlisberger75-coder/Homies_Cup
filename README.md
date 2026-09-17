# Homies Cup Mallorca 2026

PWA-Version des Auslosungs-Tools – installierbar auf iPad/iPhone/Laptop und nach dem ersten Laden auch offline nutzbar.

## Dateien

- `index.html` – App-Grundgerüst, lädt React/Babel per CDN
- `app.jsx` – die eigentliche App (Auslosung, Punkte, Tabelle) inkl. aller Teilnehmerfotos als Base64
- `manifest.json` – PWA-Manifest (Name, Icons, Farben)
- `sw.js` – Service Worker fürs Offline-Caching
- `icons/` – App-Icons in verschiedenen Grössen

## Deployment (wie beim Fussball Manager)

**Option A – Netlify Drag & Drop (am schnellsten):**
1. Auf app.netlify.com einloggen
2. Diesen ganzen Ordner per Drag & Drop auf "Sites" ziehen
3. Fertig – Netlify gibt dir eine URL

**Option B – GitHub + Netlify (für spätere Updates wie gewohnt):**
1. Neues GitHub-Repo anlegen, diese Dateien pushen
2. In Netlify "Add new site" → "Import from GitHub" → Repo auswählen
3. Bei künftigen Änderungen genügt es, `app.jsx` (und ggf. `sw.js`) zu aktualisieren und zu pushen

## Wichtig: Offline-Nutzung

Die App muss **einmal mit Internetverbindung geöffnet werden** (z. B. direkt nach dem Deployment), damit der Service Worker alle Dateien inkl. Schriftarten und React/Babel im Cache ablegt. Danach funktioniert sie auch ohne Internet – z. B. in der Ferienvilla mit schlechtem WLAN.

## Installation auf dem Homescreen

- **iPad/iPhone (Safari):** Teilen-Symbol antippen → "Zum Home-Bildschirm"
- **Android/Desktop (Chrome):** Die App zeigt automatisch ein "Installieren"-Banner an

## Wichtig: Spielstand ist pro Gerät

Da diese Version offline funktioniert, wird der Spielstand nur lokal im Browser des jeweiligen Geräts gespeichert (kein automatischer Abgleich zwischen iPad und Laptop). Nutzt am besten **ein** Gerät als "Haupt-Gerät" für die Auslosung, oder gleicht den Stand bei Bedarf über die Export/Import-Funktion (Menü → Exportieren/Importieren) ab.

## Passwort für die geheime Tabelle

`Nesslergraben`

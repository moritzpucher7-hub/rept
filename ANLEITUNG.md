# Gym-Tracker – Anleitung

Eine Web-App im iOS-Look, die du wie eine normale App auf dem iPhone-Homescreen installierst. Läuft offline, Daten bleiben nur auf deinem Handy.

## Dateien
- `index.html` – die komplette App
- `manifest.webmanifest`, `sw.js` – machen sie installierbar und offline-fähig
- `icon-*.png` – App-Icon
- `vorschau/` – Screenshots (nicht nötig zum Hosten)

## Kostenlos online stellen (GitHub Pages, ca. 5 Minuten)
1. Auf github.com kostenlos registrieren und ein neues **öffentliches** Repository anlegen, z. B. `gym`.
2. „Add file → Upload files“: `index.html`, `manifest.webmanifest`, `sw.js` und die drei `icon-*.png` hochladen, „Commit changes“.
3. Repository → **Settings → Pages** → Source: „Deploy from a branch“, Branch `main`, Ordner `/ (root)` → Save.
4. Nach ca. 1 Minute ist die App unter `https://<dein-name>.github.io/gym/` erreichbar.

Alternative ohne Konto-Setup: Ordner per Drag & Drop auf app.netlify.com/drop ziehen.

## Auf dem iPhone installieren
1. Den Link in **Safari** öffnen (nicht Chrome).
2. Teilen-Symbol → **„Zum Home-Bildschirm“** → Hinzufügen.
3. Ab jetzt über das Icon starten: Vollbild, ohne Browserleiste, funktioniert auch ohne Internet.

## Bedienung
- **Training-Tab**: deine Trainingstage. Antippen startet das heutige Training (Datum wird automatisch gesetzt, lässt sich oben antippen und ändern). Gedrückt halten oder „Bearbeiten“: Übungen verwalten, umbenennen, sortieren, löschen. „+“ legt einen neuen Tag an.
- **Im Training**: pro Übung Gewicht und Wiederholungen mit − / + einstellen (gedrückt halten zählt schnell, Zahl antippen zum Eintippen), dann „Satz speichern“. Die Werte vom letzten Mal stehen darüber und sind schon vorausgefüllt. Gewichtsschritte (0,5–5 kg) unten wählbar.
- **Verlauf-Tab**: alle Einheiten nach Monat, antippen zum Ansehen/Korrigieren. Unten Backup exportieren/importieren.

## Wichtig zu den Daten
Die Daten liegen lokal im Speicher der App auf dem iPhone. Wenn du die App vom Homescreen löschst, sind sie weg. Deshalb ab und zu im Verlauf „Backup exportieren“ (z. B. in Dateien/iCloud sichern).

## Updates
Wenn du `index.html` änderst, in `sw.js` die Zeile `const CACHE = 'gym-v1'` hochzählen (`gym-v2` …) und neu hochladen. Die App lädt die neue Version beim nächsten Öffnen mit Internet.

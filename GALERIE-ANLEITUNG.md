# DieKqikos – Galerie verwalten

Diese Homepage verwendet eine einfache Galerie ohne externe Trackingdienste. Nur berechtigte Personen mit Schreibzugriff auf das GitHub-Repository können Inhalte veröffentlichen.

## Bilder ergänzen

1. Öffne das Repository in GitHub und wähle **Add file → Upload files**.
2. Lade dein Bild in den Ordner `medien/` hoch (der Pfad muss `medien/dateiname.jpg` heißen). Bei GitHubs Weboberfläche kannst du zuerst einen Ordner anlegen oder Dateien später an die passende Stelle verschieben.
3. Öffne `galerie.json` und klicke auf das Stiftsymbol zum Bearbeiten.
4. Ergänze unter `eintraege` einen Eintrag wie:

```json
{"typ":"bild","url":"medien/bueroreinigung.jpg","titel":"Büroreinigung","beschreibung":"Einblick in ein Projekt","alt":"Gereinigter Büroraum"}
```

## Eigene Videos ergänzen

Eigene MP4-Videos können wie Bilder im Ordner `medien/` liegen. Ergänze dazu:
```json
{"typ":"video","url":"medien/renovierung.mp4","titel":"Renovierung","beschreibung":"Einblicke in die Arbeiten"}
```
**Achtung:** GitHub empfiehlt für normale Git-Repositories keine großen Binärdateien; für größere Videos sind YouTube-Links geeigneter.

## YouTube-Verlinkungen

YouTube-Videos werden nicht automatisch eingebettet. Ein Klick öffnet YouTube separat:
```json
{"typ":"youtube","url":"https://www.youtube.com/watch?v=XXXXXXXXXXX","titel":"Gartenprojekt","beschreibung":"Unser Projektvideo"}
```
Ersetze `XXXXXXXXXXX` durch die echte 11-stellige Video-ID.

## Beispiel vollständige galerie.json

```json
{
  "eintraege": [
    {"typ":"bild","url":"medien/bueroreinigung.jpg","titel":"Büroreinigung","alt":"Gereinigter Büroraum"},
    {"typ":"youtube","url":"https://www.youtube.com/watch?v=XXXXXXXXXXX","titel":"Projektvideo"}
  ]
}
```

Die Galerie lädt diese Daten über `fetch`; beim lokalen Doppelklick auf `index.html` blockieren Browser das gelegentlich. Sie funktioniert nach Veröffentlichung über einen Webserver.

## Kundenfeedback

Aktuell führt die Feedback-Schaltfläche zu einer neuen E-Mail an euch. Das ist **kein Online-Bewertungsformular** und kein automatischer öffentlicher Bewertungsfeed. Einen Link zu eurer Google-Unternehmensprofil-Bewertungsseite können wir später ergänzen, sobald ihr die konkrete Bewertungs-URL mitteilt.

## Sicherheit und Einwilligungen

Nur eigene Bilder/Videos oder solche mit Veröffentlichungserlaubnis verwenden. Für erkennbare Personen und namentlich zugeordnete Kundenstimmen die notwendigen Freigaben einholen. Keine sensiblen Objekt- oder Kundendaten sichtbar machen. Vor Livegang Impressum und Datenschutz final prüfen.

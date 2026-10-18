# Swing zu Hauf

## Neues Event anlegen
1. In `_events/` die Beispieldatei kopieren und umbenennen, z. B. `2027-06-20-sommerswing.md`.
2. Oben (zwischen den `---`) ausfüllen, darunter den freien Text schreiben. Alle Felder sind im Beispiel erklärt.
3. Uhrzeiten immer in Anführungszeichen schreiben ("18:00"), sonst versteht Jekyll sie falsch.
4. Speichern und hochladen. Das Event erscheint auf der Startseite (als "Als Nächstes"), unter "Events" und später im Archiv.

## Bilder
- Plakat: `assets/img/events/JJJJ-MM-TT/plakat.jpg` (auch .png / .webp). Webversion, ca. 1200 px breit.
- Fotos nach dem Abend: alle Bilder in `assets/img/events/JJJJ-MM-TT/fotos/`. Sie erscheinen automatisch, sortiert nach Dateiname.
  Ca. 1600 px Breite und unter 400 KB pro Bild, es gibt keine automatischen Vorschaubilder.
- Hinweis zu geplanten Fotos: Im Event `foto_vorab: true` setzen. Standardmäßig wird der Hinweis nicht angezeigt.
- Datum im Ordnernamen = Datum des Events.

## Stammdaten
- Orte: `_data/orte.yml`. Veranstalter: `_data/veranstalter.yml`. Im Event steht nur das Kürzel.
- Personen (mit Foto/Beschreibung): `_personen/kuerzel.md`. Die Beschreibung erscheint auf der Personenseite, nicht in den Besetzungskarten. Social-Media-Links können dort als Liste mit frei wählbarem Namen und URL gepflegt werden:
  ```yaml
  social_links:
    - name: Instagram
      url: https://instagram.com/beispiel
    - name: Bandcamp
      url: https://beispiel.bandcamp.com
  ```
  In der Besetzung dann `person: kuerzel`.
  Wer keine eigene Seite braucht, wird direkt mit `name:` eingetragen.
- Alle Standardtexte: `_data/texte.yml`.

## Lokal ansehen (optional)
Ruby installieren, dann im Ordner:
    bundle install
    bundle exec jekyll serve
Seite unter http://localhost:4000

## Online stellen (GitHub Pages)
Repository auf GitHub anlegen, Dateien hochladen, unter Settings > Pages "Deploy from a branch" (main, / root) wählen.
Eigene Domain: dort eintragen, beim Domainanbieter per CNAME/A-Records auf GitHub zeigen lassen.

## Hinweis
Ein Event, dessen Datum vorbei ist, wandert erst beim nächsten Neubau ins Archiv, also nach der nächsten Änderung im Repository.

## Vor dem Livegang prüfen
- `_config.yml`: E-Mail-Adresse
- `_data/orte.yml`: Adresse der Klosterkirche
- `_personen/jan-hauf.md` und `lukas-hauf.md`: Texte, ggf. Fotos
- `impressum.md` und `datenschutz.md` ausfüllen (inkl. Hinweis zu Fotos)
- `ueber-uns.md`: Platzhalterkasten durch ein Foto ersetzen: `<img src="{{ '/assets/img/brueder.jpg' | relative_url }}" alt="Jan und Lukas Hauf">`
- Beispiel-Event: nur zum Testen sichtbar machen (Zeile `published: false` löschen), dann wieder löschen
# Swing zu Hauf

## Neues Event anlegen
1. In `_events/` die Beispieldatei kopieren und umbenennen, z. B. `2027-06-20-sommerswing.md`.
2. Oben (zwischen den `---`) die Angaben ausfüllen, darunter den freien Text schreiben.
3. Speichern und hochladen. Das Event erscheint automatisch auf der Startseite (als "Als Nächstes"),
   unter "Events" und später im Archiv.

Nach dem Abend: Fotos in `assets/img/` legen und in der Event-Datei `fotos:` ergänzen.

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
- `_config.yml`: E-Mail-Adresse und die zwei Namen (bruder_schlagzeug, bruder_tanz) eintragen
- `impressum.md` und `datenschutz.md` ausfüllen
- `ueber-uns.md`: Platzhalterkasten durch ein Foto ersetzen: `<img src="{{ '/assets/img/brueder.jpg' | relative_url }}" alt="Jan und Lukas Hauf">`
- Beispiel-Event: nur zum Testen sichtbar machen (Zeile `published: false` löschen), dann wieder löschen

---
# BEISPIEL (ausgeblendet, solange 'published: false' drinsteht): kopieren, umbenennen (Datum-name.md), ausfüllen.
# Alles außer title und date ist optional. Was fehlt, wird weggelassen oder durch den Standard ersetzt.
# Uhrzeiten und Sätze immer in Anführungszeichen.
published: false   # BEISPIEL: zum Ausprobieren löschen, für echte Events nicht nötig

title: Swing im Saal
date: 2026-03-12
# untertitel: "Eigener Untertitel statt des Standardsatzes"

# --- Wo und wer ---
ort: klosterkirche-pfullingen          # Kürzel aus _data/orte.yml, oder direkt ein Text wie "Alte Halle, Stuttgart"
veranstalter: ikuh-pfullingen          # Kürzel aus _data/veranstalter.yml, oder direkt ein Name
veranstalter_seite: https://example.org/unser-abend   # Seite zum Abend beim Veranstalter (für den Dank-Satz)
# veranstalter_link: https://example.org   # nur nötig, wenn oben ein Name statt eines Kürzels steht
# dank: false                          # keinen Dank-Satz anzeigen

# --- Zeiten ---
einlass: "17:30"
beginn_kurs: "18:00"
beginn_konzert: "20:00"
# ende: "23:00"                        # nur für den Kalendereintrag

# --- Eintritt ---
eintritt: vorverkauf_abendkasse        # vorverkauf | vorverkauf_abendkasse | abendkasse | frei | offen
preis: "12 €, ermäßigt 8 €"
# eintritt_hinweis: "Kinder bis 12 frei."
tickets: https://example.org/tickets   # ohne Link führt "Okay, ich komme." auf eine Erklärseite (Abendkasse / frei / Link folgt)
# tickets_anbieter: Reservix           # sonst steht hier der Veranstalter
# status: ausverkauft                  # oder: abgesagt

# --- Tanzkurs ---
# tanzkurs: false                      # Abend ganz ohne Tanzkurs
# lukas: false                         # Lukas Hauf nicht automatisch nennen
tanzlehrer:                            # zusätzliche Gäste (Lukas kommt automatisch dazu)
  - { name: Name Tanzlehrer*in }
# tanz_text: "Eigener Satz statt „Ohne Vorkenntnisse, ohne Partner*in, ohne Angst.“"

# --- Musik ---
# Mit Live-Musik: der Satz steht in texte.yml. Nur setzen, wenn er für diesen Abend anders lauten soll.
# [[Besetzung]] wird zum Link, der nach unten zur Besetzung springt.
musik_text: "Jazz-Swing-Musik mit Jan Hauf am Schlagzeug und einem großartigen Quartett, siehe [[Besetzung]]."
band: Name der Band                    # optional, erscheint im Besetzungs-Bereich
band_link: https://example.org
# jan: false                           # Jan Hauf nicht automatisch ans Ende der Besetzung setzen
besetzung:
  - { name: Vorname Nachname, instrument: Saxofon, link: https://example.org }
  - { person: lukas-hauf, instrument: Posaune }   # Person aus _personen/ (mit Foto/Text)

# Ohne Live-Musik (dann besetzung, band und jan weglassen):
# musik: ohne
# musik_text: "Heute legt Lukas die Platten auf."                           # sonst: "Swing-Musik aus der Box."
# musik_hinweis: "Ausnahmsweise ohne Band. Beim nächsten Mal wieder live."  # sonst: der Augenzwinker-Satz

# --- Extras: beliebig viele Zeilen (zeit und titel optional, text darf Markdown enthalten) ---
extras:
  - { zeit: Zwischendurch, titel: Gedankenpause, text: "Ein kurzer philosophischer Exkurs über ..." }

# --- Bilder: nur Ordner anlegen, nichts eintragen ---
#   Plakat: assets/img/events/2027-03-12/plakat.jpg
#   Fotos:  assets/img/events/2027-03-12/fotos/
# foto_vorab: true                       # Hinweis zu geplanten Fotos anzeigen (Standard: aus)
# plakat_alt: "Plakat mit Besetzung, Datum, Ort und Uhrzeiten"
# fotos_credit: "Name der Fotografin / des Fotografen"
---
Hier steht der freie Text zum Abend: was euch erwartet, Hinweise zur Anreise. Markdown funktioniert, also **fett**, *kursiv* und [Links](https://example.org).
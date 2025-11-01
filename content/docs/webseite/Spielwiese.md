---
title: "Spielwiese"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Spielwiese

dev/test Stage der Hauptseite [erfindergeist.org](https://erfindergeist.org)

## Einspielen von PROD

Hinweis: das backup tool hat limits beim upload, daher müssen wir ein paar Umwege gehen.

- auf prod: im admin Bereich: all-in-one-migration: export, ohne Medien Dateien, in Datei anstoßen
- auf spielwiese: im admin Bereich: all-in-one-migration: vorherigen export hochladen und bereitstellen.
- auf spielwiese: im admin Bereich: einstellungen: Untertitel "DEV" hinzufügen
- FTP Prod: von "wpmain/wp-content/uploads/" alle vollen Jahreszahlen Ordner (2024, 2025..) runter laden und entsprechend bei spielwiese hochladen
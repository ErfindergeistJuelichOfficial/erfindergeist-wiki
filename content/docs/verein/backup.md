---
title: "Backup Konzept"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

Es sollte folgende Reihenfolge eingehalten werden weil backups aufeinander aufbauen

## Webseite

Die Webseite nutzt Wordpress. Im April 2023 wurde in einer Website Team Sitzung das Plugin [All-in-One WP Migration and Backup](https://wordpress.org/plugins/all-in-one-wp-migration/) gewählt um Backups zu erstellen.

Das Backup wird nach Erstellung in M365 unter [Vorstand/bckupWebsite](https://erfindergeist.sharepoint.com/sites/Vorstand/bckupWebsite) abgelegt.

## E-Mails

keine Backps. Wichtige Mails bitte in den Ordnern speichern.

## HomeAssistant

TODO

## GIT

TODO

### ideas

 ```bash
gh auth login
gh repo list ErfindergeistJuelichOfficial --json name,url,visibility > out.json  
```

## M365

Es werden nur Dokumentenbibliotheken (DocLib)  OHNE Metadaten gesichert!
Folgende DocLibs werden gesichert:

- [Vorstand/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Vorstand/Freigegebene%20Dokumente/)
- [Vorstand/Mitgliederantrge](https://erfindergeist.sharepoint.com/sites/Vorstand/Mitgliederantrge)
- [Vorstand/bckupWebsite](https://erfindergeist.sharepoint.com/sites/Vorstand/bckupWebsite)
- [Team/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Team/Freigegebene%20Dokumente)
- [Mitglieder/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Mitglieder/Freigegebene%20Dokumente)
- [Mitglieder/Plenen](https://erfindergeist.sharepoint.com/sites/Mitglieder/Plenen) (Metadaten zur Sortierung)
- [Mitglieder/Rechnungen](https://erfindergeist.sharepoint.com/sites/Mitglieder/Rechnungen) (Metadaten zur Sortierung)
- [Marketing/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Marketing/Freigegebene%20Dokumente)
- [Repaircafe/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Repaircafe/Freigegebene%20Dokumente)

Der einfachste Weg ist die DocLibs via oneDrive immer auf einen Windows Rechner zu Synchronisieren (Dateien immer auf diesem Gerät behalten) und davon ein Backup erstellen

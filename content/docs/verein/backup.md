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
# Backup Konzept

Es sollte folgende reihenfolge eingehalten werden weil backups aufeinander aufbauen

## Webseite

Die Webseite nutzt Wordpress. Im April 2023 wurde in einer Website Team Sitzung das Plugin [All-in-One WP Migration and Backup](https://wordpress.org/plugins/all-in-one-wp-migration/) gewählt um Backups zu erstellen.

Das Backup wird nach Erstellung in M365 unter [Vorstand/bckupWebsite](https://erfindergeist.sharepoint.com/sites/Vorstand/bckupWebsite) abgelegt.

## E-Mails

TODO aktuelle keine backups

wichtig wäre
kontakt@e...org
vorstand@e...org

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
folgende DocLibs werden gesichert:

- [Vorstand/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Vorstand/Freigegebene%20Dokumente/)
- [Vorstand/Mitgliederantrge](https://erfindergeist.sharepoint.com/sites/Vorstand/Mitgliederantrge)
- [Vorstand/bckupWebsite](https://erfindergeist.sharepoint.com/sites/Vorstand/bckupWebsite)
- [Team/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Team/Freigegebene%20Dokumente)
- [Mitglieder/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Mitglieder/Freigegebene%20Dokumente)
- [Mitglieder/Plenen](https://erfindergeist.sharepoint.com/sites/Mitglieder/Plenen) (Metadaten zur Sortierung)
- [Mitglieder/Rechnungen](https://erfindergeist.sharepoint.com/sites/Mitglieder/Rechnungen) (Metadaten zur Sortierung)
- [Marketing/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Marketing/Freigegebene%20Dokumente)
- [Repaircafe/Freigegebene%20Dokumente](https://erfindergeist.sharepoint.com/sites/Repaircafe/Freigegebene%20Dokumente)

Der einfachste weg ist die DocLibs via oneDrive immer auf einen windows Rechner zu Synchronisieren (Dateien immer auf diesem Gerät behalten) und davon ein backup erstellen
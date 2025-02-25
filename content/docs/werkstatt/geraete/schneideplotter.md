---
title: "Schneideplotter"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---
# Schneideplotter

- SeikiTech
- Bezeichnung: TODO

## Schutzvorkehrungen

TODO

## Einschaltung

Stecker einstecken

## Ausschaltung

Stecker ziehen

## Bedienungsanleitung

### Einstellungen am Gerät

Zuerst wird die Folie eingelegt. Dazu die beiden Rollen über die Hebel anheben, die
Folie einlegen und ausrichten.

Nun kann der Ursprung, also der Startpunkt des Schneidekopfes und der Folie festgelegt werden.
Dazu drückt man den Knopf `Leave`.

![Verlassen](/images/schneideplotter/leave.jpg)

Der Kopf und die Folie kann frei über die Pfeiltasten bewegt werden.

![Achsen bewegen](/images/schneideplotter/move.jpg)

Wenn der Kopf und die Folie ausgerichtet sind, kann man den Ursprung über den Knopf `Origin` übernehmen.

![Origin festlegen](/images/schneideplotter/origin.jpg)

Dann kann über den Knopf `Setting` die Geschwindigkeit mit den rechts/links Knöpfen und der Druck über die hoch/runter Knöpfe eingestellt werden. Als gute Starteinstellung empfiehlt sich 130 mm/s Geschwindigkeit und 300g Druck.

### Ansteuerung über Inkscape

Die Software [Inkscape](https://inkscape.org/de/) bietet native Unterstützung für Schneideplotter.

Dafür wird das Objekt zuerst in Inkscape modelliert oder importiert.
Dann muss das Objekt in einen Pfad konvertiert werden. Dazu wird das Objekt ausgewählt und über das Menü `Path` > `Object to Path` konvertiert.

![Pfad](/images/schneideplotter/path.png)

Nun kann der Plotter mit einem USB-A Kabel an den Rechner verbunden und eingeschaltet werden.
Anschließend in Inkscape das ganze Objekt auswählen und das Menü `Extensions` > `Export` > `Plot...` öffnen.
Hier muss der richtige Port ausgewählt werden. In Linux kann mit `dmesg` herausgefunden werden, an welchem Port das Gerät registriert wurde. Beispielsweise `/dev/ttyUSB0`. Dafür muss auch `Parallel` ausgewählt sein. Außerdem muss vorher unter Linux sichergestellt sein, dass der Nutzer Mitglied in der Gruppe `dialout` ist.

![Anwenden](/images/schneideplotter/apply.png)

### Prozess starten

Den Rest der Einstellungen muss eigentlich nicht geändert werden. Nun kann über `Apply` der Schneideplotter gestartet werden.

Hier das Ergebnis dieses sehr einfachen Musters.

![Ergebnis](/images/schneideplotter/result.jpg)

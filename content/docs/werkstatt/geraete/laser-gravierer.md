---
title: "Laser Gravierer"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---
# Laser Gravierer

- Laser Pecker
- LP4
[Produkt Webseite](https://de.laserpecker.net/products/laserpecker-4)

## Schutzvorkehrungen

> - Laser-Schutz-Brille anziehen
> - Laser-Schutz-Gehäuse verwenden falls möglich
> - Personen ohne Laser-Schutz-Brille aus dem Raum verweisen

## Dokumente

TODO

## Zubehör

- [Drehvorrichtung](https://de.laserpecker.net/products/rotary-extension)
- [Schiebeverlängerung](https://de.laserpecker.net/products/preorder-laserpecker-4-slide-extension)
- [Schneidplatte](https://de.laserpecker.net/products/preorder-laserpecker-4-cutting-plate)
- [Luftreiniger](https://de.laserpecker.net/products/laserpecker-air-purifier)
- 2x Schutzbrille

## Einschaltung

- Stromkabel von Drucker und Filter einstecken
- Der Filter muss durch drücken des Plus-Buttons aktiviert werden. Die Stärke muss selber angepasst werden
- während Pausen kann man durch gedrückt halten der Minus-Taste für 5sec, den Filter ausschalten

## Ausschaltung

- Einfach beide Netz-Stecker ziehen.

## Bedienungsanleitung

### Software

Der Drucker ist nur via Bluetooth nutzbar. Am einfachsten ist die Smartphone Software zu nutzen. PC Software läuft nur auf Windows oder Mac und wurde noch nicht getestet. im Zubehör liegt eine Bluetooth Dongle für PC-Systeme ohne Bluetooth

### Smartphone App

<https://de.laserpecker.net/pages/app>

Empfehlung: LaserPecker Design Space

### PC Software

<https://de.laserpecker.net/pages/software>

### LaserPecker Design Space

- Bild wählen und auf Vorschau drücken.
- In der Vorschau kann man das zu bedruckende Werkstück ausrichten oder das Bild in der App drehen bzw. die Größe ändern
- Danach soll man eine Auflösung wählen. Beim testen viel auf, je höher die Auflösung je tiefer geht der Laser.
- Im Folge Screen kann man das Material wählen. Was Dazu führt das Stärke und tiefe automatisch eingestellt werden.
- Ab hier muss man sich an die perfekte einstellung ran tasten.

### InkScape

folgend optimale Einstellungen zum Schneiden:

- Objekte:
  - Fill: "no paint" ![InkScape1](/images/laser-gravierer/test_1_inkScape_01.png)
  - Stroke paint: "black" ![InkScape2](/images/laser-gravierer/test_1_inkScape_02.png)
  - Stroke style: "0,4mm, solid line" ![InkScape3](/images/laser-gravierer/test_1_inkScape_03.png)
- als PNG mit 300 DPI exportieren

### Tests

#### Schneiden

Da keine geeigneten einstellungen zum schneiden gefunden wurden, wurden tests durchgeführt. folgend dokumentiert

##### Test Datei

Zum testen wurde folgende Datei verwendet:

SVG:

![Test_Datei_SVG](/images/laser-gravierer/circle00C.svg)

PNG:

![Test_Datei_PNG](/images/laser-gravierer/circle00C.png)

###### Test 1

- Holz:
  - Material: Lindenholz
  - Holzstärke 2mm ? (prüfen)
- InkScape:
  - Optimale Linien dicke in InkScape: 0,3mm - 0,4mm
- Drucker:
  - Auflösung 4k
  - Laser Stärke: 25%
  - Laser Tiefe: 80%

0,3 musste man leicht drücken und raus brechen hatte aber keine Brandspuren. bei 0,4 gab es leichte Brandspuren

![test_1_ergebnis](/images/laser-gravierer/test_ergebnis_1.jpg)


---
title: "Room-Status-wp-plugin"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Room-Status-wp-plugin

- Code: [GitHub](https://github.com/ErfindergeistJuelichOfficial/room-status-wp-plugin)
- Alle Daten werden Stündlich aktualisiert.
- Es gibt einige Sensoren wie Wasser, Rauch, Schlößer und Bewegung welche bei status änderung sofort aktualisiert werden.
- Es können keine Daten an den Raum gesendet werden.
- Wer möchte kann sich damit einen Dashboard für zuhause bauen. Wir freuen uns auf Beiträge von euch.

## Einige Mappings mit Fakten

| key | gerät | Zone | Beschreibung |
|--|--|--|--|
| sensorA5A8... | Xiaomi MI Thermometer V2 | IT-Ecke | Temperatur, Luftfeuchte Batterie|
| sensorA4F0... | Xiaomi MI Thermometer V2 | Tischbohrmaschine | Temperatur, Luftfeuchte Batterie |
| currentMeterNetworkEnergy | Shelly PM Mini Gen3 | Netzwerk-Schrank | Gesamte kWh Verbrauch der Netzwerk-Schrank seit 1.6.2024 |
| plugPrusaEnergy | TP-Link Tapo P110M Matter | Steckdose 3D-Drucker2 (Prusa-Core-One) | Gesamt kWh Verbrauch des Druckers seit 1.10.2025 |

## curl example

```bash
curl -X GET https://erfindergeist.org/wp-json/erfindergeist/v2/room-status
```

## example data

```json
{
  "lockWorkshopState": {
    "value": "locked",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "lockWorkshopBattery": {
    "value": "94",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "lockFrontDoorBattery": {
    "value": "88",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "lockAWOBattery": {
    "value": "62",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "doorState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "doorIlluminance": {
    "value": "0.0",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "doorBattery": {
    "value": "100",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA5A8Humidity": {
    "value": "62.66",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA5A8Temperature": {
    "value": "18.67",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA5A8Battery": {
    "value": "84",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA4F0Humidity": {
    "value": "58.79",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA4F0Temperature": {
    "value": "18.91",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "sensorA4F0Battery": {
    "value": "72",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "smokeAlertState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "smokeAlertBattery": {
    "value": "86",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "floodAlertState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "floodAlertTemperature": {
    "value": "17.75",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "floodAlertBattery": {
    "value": "100",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "currentMeterNetworkCurrent": {
    "value": "0.267",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "currentMeterNetworkEnergy": {
    "value": "281.149963",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "currentMeterNetworkPower": {
    "value": "33.8",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "currentMeterNetworkVoltage": {
    "value": "238.8",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "camPersonAlertState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "camAnimalAlertState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "camMotionAlertState": {
    "value": "off",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "homeassistantCoreCPU": {
    "value": "0.56",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "homeassistantCoreRAM": {
    "value": "5.95",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "plugPrusaEnergy": {
    "value": "1.631",
    "dateTime": "2025-10-04T10:35:50+00:00"
  },
  "prusaState": {
    "value": "finished",
    "dateTime": "2025-10-04T10:35:50+00:00"
  }
}

```

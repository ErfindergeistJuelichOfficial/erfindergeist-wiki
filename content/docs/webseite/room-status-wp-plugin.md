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

- [GitHub](https://github.com/ErfindergeistJuelichOfficial/room-status-wp-plugin)
- Alle Daten werden Stündlich aktualisiert.
- es gibt einige Sensoren wir Wasser, Rauch, Schlößer und Bewegung welche bei status änderung sofort aktualisiert werden.
- Es können keine Daten an den Raum gesendet werden.
- Wer möchte kann sich damit einen Dashboard für zuhause bauen. Wir freuen uns auf Beiträge von euch.

## curl example

```bash
curl -X GET https://erfindergeist.org/wp-json/erfindergeist/v2/room-status
```

## example data

```json
{
    "lockWorkshopState": {
        "value": "locked",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "lockWorkshopBattery": {
        "value": "96",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "lockFrontDoorBattery": {
        "value": "88",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "lockAWOBattery": {
        "value": "62",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "doorState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "doorIlluminance": {
        "value": "8.0",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "doorBattery": {
        "value": "100",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA5A8Humidity": {
        "value": "57.1",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA5A8Temperature": {
        "value": "19.01",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA5A8Battery": {
        "value": "91",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA4F0Humidity": {
        "value": "53.79",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA4F0Temperature": {
        "value": "18.96",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "sensorA4F0Battery": {
        "value": "72",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "smokeAlertState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "smokeAlertBattery": {
        "value": "86",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "floodAlertState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "floodAlertTemperature": {
        "value": "17.25",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "floodAlertBattery": {
        "value": "100",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "currentMeterNetworkCurrent": {
        "value": "0.277",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "currentMeterNetworkEnergy": {
        "value": "279.584488",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "currentMeterNetworkPower": {
        "value": "34.1",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "currentMeterNetworkVoltage": {
        "value": "240.0",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "camPersonAlertState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "camAnimalAlertState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "camMotionAlertState": {
        "value": "off",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "homeassistantCoreCPU": {
        "value": "0.47",
        "dateTime": "2025-10-02T14:00:00+00:00"
    },
    "homeassistantCoreRAM": {
        "value": "5.86",
        "dateTime": "2025-10-02T14:00:00+00:00"
    }
}
```

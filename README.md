# Marstek Venus E – Zero Export Controller V4.2

Home Assistant Blueprint zur externen Steuerung eines Marstek Venus E via RS485/Modbus mit dem Ziel, Einspeisung möglichst nahe an 0 W zu regeln.

## Features

- RS485-Steuermodus aktivieren
- Strategie auf `Manuell` setzen
- Force-Mode auf `Halt`, `Laden`, `Entladen` setzen
- Lade- und Entladeleistung regeln
- SOC-Schutz
- Umschalt-Cooldown
- Hysterese mit getrennten Start-/Stop-Schwellen
- optionaler PV-Zwang für Laden
- optionale Abendfreigabe für Entladen
- optionales Grid-Smoothing
- optionales Night-Profile
- Debug-Helfer für Diagnose

---

## Voraussetzungen

Benötigt werden passende Home-Assistant-Entities für:

- Grid Power Sensor
- Battery SOC Sensor
- PV Power Sensor
- Marstek Strategy Select
- Marstek Action Select
- RS485 Switch
- Charge Power Number
- Discharge Power Number
- Max Charge Power Number
- Max Discharge Power Number
- Max SOC Number

Zusätzlich werden mehrere Helper benötigt.

---

## Projektstruktur

```text
blueprints/
└── automation/
    └── marstek/
        ├── marstek_venus_zero_export_controller_v4_2.yaml
        └── README.md

packages/
└── marstek/
    ├── helpers.yaml
    ├── template_sensors.yaml
    └── dashboard_marstek.yaml

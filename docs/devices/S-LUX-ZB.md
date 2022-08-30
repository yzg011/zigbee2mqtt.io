---
title: "TuYa S-LUX-ZB control via MQTT"
description: "Integrate your TuYa S-LUX-ZB via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-08-01T20:41:55Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa S-LUX-ZB

|     |     |
|-----|-----|
| Model | S-LUX-ZB  |
| Vendor  | TuYa  |
| Description | Light sensor |
| Exposes | battery, illuminance_lux, linkquality, brightness_level |
| Picture | ![TuYa S-LUX-ZB](https://www.zigbee2mqtt.io/images/devices/S-LUX-ZB.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Illuminance_lux (numeric)
Measured illuminance in lux.
Value can be found in the published state on the `illuminance_lux` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `lx`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

### Brightness_level (enum)
Value can be found in the published state on the `brightness_level` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `LOW`, `MEDIUM`, `HIGH`.


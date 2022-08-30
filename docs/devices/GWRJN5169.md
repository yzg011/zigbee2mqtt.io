---
title: "OpenLumi GWRJN5169 control via MQTT"
description: "Integrate your OpenLumi GWRJN5169 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-01-26T20:08:21Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# OpenLumi GWRJN5169

|     |     |
|-----|-----|
| Model | GWRJN5169  |
| Vendor  | OpenLumi  |
| Description | [Lumi Router (JN5169)](https://github.com/igo-r/Lumi-Router-JN5169) |
| Exposes | device_temperature, linkquality |
| Picture | ![OpenLumi GWRJN5169](https://www.zigbee2mqtt.io/images/devices/GWRJN5169.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Firmware
Zigbee Router for __Xiaomi DGNWG05LM__ and __Aqara ZHWG11LM__ gateways.

Open source firmware can be found here: [Github](https://github.com/igo-r/Lumi-Router-JN5169)
<!-- Notes END: Do not edit below this line -->



## Exposes

### Device_temperature (numeric)
Temperature of the device.
Value can be found in the published state on the `device_temperature` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `°C`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


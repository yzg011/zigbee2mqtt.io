---
title: "SONOFF S26R2ZB control via MQTT"
description: "Integrate your SONOFF S26R2ZB via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-10-01T17:18:02Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# SONOFF S26R2ZB

|     |     |
|-----|-----|
| Model | S26R2ZB  |
| Vendor  | SONOFF  |
| Description | Zigbee smart plug |
| Exposes | switch (state), linkquality |
| Picture | ![SONOFF S26R2ZB](https://www.zigbee2mqtt.io/images/devices/S26R2ZB.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### Pairing

If brand new, the device will enter the pairing mode during the first use and the LED signal indicator flashes. If not (or if has been paired before and needs to be re-paired) - press and hold the pairing/power button for about 5 seconds until the LED signal indicator flashes and release, then the device enters pairing mode.
<!-- Notes END: Do not edit below this line -->



## Exposes

### Switch 
The current state of this switch is in the published state under the `state` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "ON"}`, `{"state": "OFF"}` or `{"state": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


---
title: "SONOFF S40ZBTPB control via MQTT"
description: "Integrate your SONOFF S40ZBTPB via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-07-01T08:15:09
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# SONOFF S40ZBTPB

|     |     |
|-----|-----|
| Model | S40ZBTPB  |
| Vendor  | SONOFF  |
| Description | 15A Zigbee smart plug |
| Exposes | switch (state), linkquality |
| Picture | ![SONOFF S40ZBTPB](https://www.zigbee2mqtt.io/images/devices/S40ZBTPB.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### Pairing
After first power on, it should enter pairing mode. To pair to a new network, long press reset button for 5s until the Wi-Fi LED indicator changes to a cycle of two short flashes and one long flash, then release.
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


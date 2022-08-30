---
title: "SONOFF BASICZBR3 control via MQTT"
description: "Integrate your SONOFF BASICZBR3 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2019-11-09T18:37:38Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# SONOFF BASICZBR3

|     |     |
|-----|-----|
| Model | BASICZBR3  |
| Vendor  | SONOFF  |
| Description | Zigbee smart switch |
| Exposes | switch (state), linkquality |
| Picture | ![SONOFF BASICZBR3](https://www.zigbee2mqtt.io/images/devices/BASICZBR3.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
If brand new, when powered on it will attempt to pair to Zigbee2MQTT automatically. If not (or if has been paired before and needs to be re-paired) - press and hold the (relay) button on the top for about 5 seconds until the relay clicks and the red LED flashes several times. The device will then go into pairing mode and the blue LED will begin to flash. When connected, the blue LED will turn on solid. It should then be connected to Zigbee2MQTT. Pressing the button should activate the relay on/off as normal, and the red LED will be on/off.
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


---
title: "eWeLink SA-003-Zigbee control via MQTT"
description: "Integrate your eWeLink SA-003-Zigbee via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2019-12-15T17:27:48Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# eWeLink SA-003-Zigbee

|     |     |
|-----|-----|
| Model | SA-003-Zigbee  |
| Vendor  | eWeLink  |
| Description | Zigbee smart plug |
| Exposes | switch (state), linkquality |
| Picture | ![eWeLink SA-003-Zigbee](https://www.zigbee2mqtt.io/images/devices/SA-003-Zigbee.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
Reset by unplugging any devices plugged into the socket, hold the button down for 10 secs until the light flashes Green/Orange and the Socket switches on and off. pair within 60 secs
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


---
title: "Nue / 3A HGZB-42-UK / HGZB-41 / HGZB-41-UK control via MQTT"
description: "Integrate your Nue / 3A HGZB-42-UK / HGZB-41 / HGZB-41-UK via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2019-12-15T17:27:48Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Nue / 3A HGZB-42-UK / HGZB-41 / HGZB-41-UK

|     |     |
|-----|-----|
| Model | HGZB-42-UK / HGZB-41 / HGZB-41-UK  |
| Vendor  | Nue / 3A  |
| Description | Smart switch 1 or 2 gang |
| Exposes | switch (state), linkquality |
| Picture | ![Nue / 3A HGZB-42-UK / HGZB-41 / HGZB-41-UK](https://www.zigbee2mqtt.io/images/devices/HGZB-42-UK---HGZB-41---HGZB-41-UK.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


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


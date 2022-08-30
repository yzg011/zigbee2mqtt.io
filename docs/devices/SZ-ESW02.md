---
title: "Sercomm SZ-ESW02 control via MQTT"
description: "Integrate your Sercomm SZ-ESW02 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2019-11-09T18:37:38Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Sercomm SZ-ESW02

|     |     |
|-----|-----|
| Model | SZ-ESW02  |
| Vendor  | Sercomm  |
| Description | Telstra smart plug 2 |
| Exposes | switch (state), power, linkquality |
| Picture | ![Sercomm SZ-ESW02](https://www.zigbee2mqtt.io/images/devices/SZ-ESW02.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
With the device unplugged (or socket switched off), press and hold the pairing button for ~4 seconds. Continue holding the pairing button while plugging in the device (or switching the socket on) and continue to hold while the LED has been illuminated (in 4 seconds). The sensor shall the wipe any knowledge of the previous network and other configuration parameters and begin searching for a new network (Auto Joining State).
<!-- Notes END: Do not edit below this line -->



## Exposes

### Switch 
The current state of this switch is in the published state under the `state` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "ON"}`, `{"state": "OFF"}` or `{"state": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.

### Power (numeric)
Instantaneous measured power.
Value can be found in the published state on the `power` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


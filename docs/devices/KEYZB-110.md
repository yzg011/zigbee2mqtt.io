---
title: "Develco KEYZB-110 control via MQTT"
description: "Integrate your Develco KEYZB-110 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-10-30T12:58:50
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Develco KEYZB-110

|     |     |
|-----|-----|
| Model | KEYZB-110  |
| Vendor  | Develco  |
| Description | Keypad |
| Exposes | battery, battery_low, voltage, tamper, action_code, action_transaction, action_zone, action, linkquality |
| Picture | ![Develco KEYZB-110](https://www.zigbee2mqtt.io/images/devices/KEYZB-110.jpg) |
| White-label | Frient KEPZB-110 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->

## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).



## Exposes

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Battery_low (binary)
Indicates if the battery of this device is almost empty.
Value can be found in the published state on the `battery_low` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` battery_low is ON, if `false` OFF.

### Voltage (numeric)
Voltage of the battery in millivolts.
Value can be found in the published state on the `voltage` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `mV`.

### Tamper (binary)
Indicates whether the device is tampered.
Value can be found in the published state on the `tamper` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` tamper is ON, if `false` OFF.

### Action_code (text)
Pin code introduced..
Value can be found in the published state on the `action_code` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Action_transaction (numeric)
Last action transaction number..
Value can be found in the published state on the `action_transaction` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Action_zone (text)
Alarm zone. Default value 23.
Value can be found in the published state on the `action_zone` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Action (enum)
Triggered action (e.g. a button click).
Value can be found in the published state on the `action` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `disarm`, `arm_day_zones`, `arm_night_zones`, `arm_all_zones`, `exit_delay`, `emergency`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


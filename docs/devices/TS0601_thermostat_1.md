---
title: "TuYa TS0601_thermostat_1 control via MQTT"
description: "Integrate your TuYa TS0601_thermostat_1 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-10-30T12:58:50
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa TS0601_thermostat_1

|     |     |
|-----|-----|
| Model | TS0601_thermostat_1  |
| Vendor  | TuYa  |
| Description | Thermostatic radiator valve |
| Exposes | battery, lock (state), max_temperature, min_temperature, position, switch (state), window, heating, climate (local_temperature, current_heating_setpoint, local_temperature_calibration, preset), programming_mode, boost_heating, boost_heating_countdown, linkquality |
| Picture | ![TuYa TS0601_thermostat_1](https://www.zigbee2mqtt.io/images/devices/TS0601_thermostat_1.jpg) |
| White-label | Unknown/id3.pl GTZ06 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Lock 
The current state of this lock is in the published state under the `child_lock` property (value is `LOCK` or `UNLOCK`).
To control this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"child_lock": "LOCK"}` or `{"child_lock": "UNLOCK"}`.
It's not possible to read (`/get`) this value.

### Max_temperature (numeric)
Maximum temperature.
Value can be found in the published state on the `max_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"max_temperature": NEW_VALUE}`.
The minimal value is `15` and the maximum value is `35`.
The unit of this value is `°C`.

### Min_temperature (numeric)
Minimum temperature.
Value can be found in the published state on the `min_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"min_temperature": NEW_VALUE}`.
The minimal value is `1` and the maximum value is `15`.
The unit of this value is `°C`.

### Position (numeric)
Position.
Value can be found in the published state on the `position` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `%`.

### Switch 
The current state of this switch is in the published state under the `window_detection` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"window_detection": "ON"}`, `{"window_detection": "OFF"}` or `{"window_detection": "TOGGLE"}`.
It's not possible to read (`/get`) this value.

### Window (binary)
Window status closed or open .
Value can be found in the published state on the `window` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `CLOSED` window is ON, if `OPEN` OFF.

### Heating (binary)
Device valve is open or closed (heating or not).
Value can be found in the published state on the `heating` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `ON` heating is ON, if `OFF` OFF.

### Climate 
This climate device supports the following features: `local_temperature`, `current_heating_setpoint`, `local_temperature_calibration`, `preset`.
- `current_heating_setpoint`: Temperature setpoint. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"current_heating_setpoint": VALUE}` where `VALUE` is the °C between `5` and `35`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"current_heating_setpoint": ""}`.
- `local_temperature`: Current temperature measured on the device (in °C). Reading (`/get`) this attribute is not possible.
- `preset`: MANUAL MODE ☝ - In this mode, the device executes manual temperature setting. When the set temperature is lower than the "minimum temperature", the valve is closed (forced closed). AUTO MODE ⏱ - In this mode, the device executes a preset week programming temperature time and temperature. ON - In this mode, the thermostat stays open OFF - In this mode, the thermostat stays closed. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"preset": VALUE}` where `VALUE` is one of: `auto`, `manual`, `off`, `on`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"preset": ""}`.
- `local_temperature_calibration`: Offset to be used in the local_temperature. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"local_temperature_calibration": VALUE}.`

### Programming_mode (composite)
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"undefined": {"monday_schedule": VALUE, "tuesday_schedule": VALUE, "wednesday_schedule": VALUE, "thursday_schedule": VALUE, "friday_schedule": VALUE, "saturday_schedule": VALUE, "sunday_schedule": VALUE}}`
- `monday_schedule` (text): undefined. 
- `tuesday_schedule` (text): undefined. 
- `wednesday_schedule` (text): undefined. 
- `thursday_schedule` (text): undefined. 
- `friday_schedule` (text): undefined. 
- `saturday_schedule` (text): undefined. 
- `sunday_schedule` (text): undefined. 

### Boost_heating (binary)
Boost Heating: press and hold "+" for 3 seconds, the device will enter the boost heating mode, and the ▷╵◁ will flash. The countdown will be displayed in the APP.
Value can be found in the published state on the `boost_heating` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"boost_heating": NEW_VALUE}`.
If value equals `ON` boost_heating is ON, if `OFF` OFF.

### Boost_heating_countdown (numeric)
Countdown in minutes.
Value can be found in the published state on the `boost_heating_countdown` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"boost_heating_countdown": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `1000`.
The unit of this value is `min`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


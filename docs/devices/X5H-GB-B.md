---
title: "TuYa X5H-GB-B control via MQTT"
description: "Integrate your TuYa X5H-GB-B via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-08-01T15:06:58
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa X5H-GB-B

|     |     |
|-----|-----|
| Model | X5H-GB-B  |
| Vendor  | TuYa  |
| Description | Wall-mount thermostat |
| Exposes | climate (current_heating_setpoint, local_temperature, local_temperature_calibration, system_mode, running_state, preset, sensor), schedule, lock (state), week, brightness_state, sound, frost_protection, factory_reset, heating_temp_limit, deadzone_temperature, upper_temp, linkquality |
| Picture | ![TuYa X5H-GB-B](https://www.zigbee2mqtt.io/images/devices/X5H-GB-B.jpg) |
| White-label | Beok TGR85-ZB |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Climate 
This climate device supports the following features: `current_heating_setpoint`, `local_temperature`, `local_temperature_calibration`, `system_mode`, `running_state`, `preset`, `sensor`.
- `current_heating_setpoint`: Temperature setpoint. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"current_heating_setpoint": VALUE}` where `VALUE` is the °C between `5` and `60`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"current_heating_setpoint": ""}`.
- `local_temperature`: Current temperature measured on the device (in °C). Reading (`/get`) this attribute is not possible.
- `system_mode`: Mode of this device. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"system_mode": VALUE}` where `VALUE` is one of: `off`, `heat`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"system_mode": ""}`.
- `preset`: Mode of this device (similar to system_mode). To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"preset": VALUE}` where `VALUE` is one of: `manual`, `program`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"preset": ""}`.
- `running_state`: The current running state. Possible values are: `idle`, `heat`. To read send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"running_state": ""}`.
- `local_temperature_calibration`: Offset to be used in the local_temperature. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"local_temperature_calibration": VALUE}.`

### Schedule (text)
Value can be found in the published state on the `schedule` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"schedule": NEW_VALUE}`.

### Lock 
The current state of this lock is in the published state under the `child_lock` property (value is `LOCK` or `UNLOCK`).
To control this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"child_lock": "LOCK"}` or `{"child_lock": "UNLOCK"}`.
It's not possible to read (`/get`) this value.

### Week (enum)
Week format user for schedule.
Value can be found in the published state on the `week` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"week": NEW_VALUE}`.
The possible values are: `5+2`, `6+1`, `7`.

### Brightness_state (enum)
Screen brightness.
Value can be found in the published state on the `brightness_state` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"brightness_state": NEW_VALUE}`.
The possible values are: `off`, `low`, `medium`, `high`.

### Sound (binary)
Switches beep sound when interacting with thermostat.
Value can be found in the published state on the `sound` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"sound": NEW_VALUE}`.
If value equals `ON` sound is ON, if `OFF` OFF.

### Frost_protection (binary)
Antifreeze function.
Value can be found in the published state on the `frost_protection` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"frost_protection": NEW_VALUE}`.
If value equals `ON` frost_protection is ON, if `OFF` OFF.

### Factory_reset (binary)
Resets all settings to default. Doesn't unpair device..
Value can be found in the published state on the `factory_reset` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"factory_reset": NEW_VALUE}`.
If value equals `ON` factory_reset is ON, if `OFF` OFF.

### Heating_temp_limit (numeric)
Heating temperature limit.
Value can be found in the published state on the `heating_temp_limit` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"heating_temp_limit": NEW_VALUE}`.
The minimal value is `5` and the maximum value is `60`.
The unit of this value is `°C`.
Besides the numeric values the following values are accepected: `default`.

### Deadzone_temperature (numeric)
The delta between local_temperature and current_heating_setpoint to trigger Heat.
Value can be found in the published state on the `deadzone_temperature` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"deadzone_temperature": NEW_VALUE}`.
The minimal value is `0.5` and the maximum value is `9.5`.
The unit of this value is `°C`.
Besides the numeric values the following values are accepected: `default`.

### Upper_temp (numeric)
Value can be found in the published state on the `upper_temp` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"upper_temp": NEW_VALUE}`.
The minimal value is `35` and the maximum value is `95`.
The unit of this value is `°C`.
Besides the numeric values the following values are accepected: `default`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


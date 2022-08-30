---
title: "Perenio PEHPL0X control via MQTT"
description: "Integrate your Perenio PEHPL0X via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-06-01T15:08:55
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Perenio PEHPL0X

|     |     |
|-----|-----|
| Model | PEHPL0X  |
| Vendor  | Perenio  |
| Description | Power link |
| Exposes | switch (state), default_on_off_state, rms_voltage, active_power, consumed_energy, alarm_voltage_min, alarm_voltage_max, alarm_power_max, rssi, linkquality |
| Picture | ![Perenio PEHPL0X](https://www.zigbee2mqtt.io/images/devices/PEHPL0X.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Switch 
The current state of this switch is in the published state under the `state` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "ON"}`, `{"state": "OFF"}` or `{"state": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.

### Default_on_off_state (enum)
Value can be found in the published state on the `default_on_off_state` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"default_on_off_state": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"default_on_off_state": NEW_VALUE}`.
The possible values are: `on`, `off`, `previous`.

### Rms_voltage (numeric)
RMS voltage.
Value can be found in the published state on the `rms_voltage` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `V`.

### Active_power (numeric)
Active power.
Value can be found in the published state on the `active_power` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W`.

### Consumed_energy (numeric)
Consumed energy.
Value can be found in the published state on the `consumed_energy` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W*h`.

### Alarm_voltage_min (binary)
Indicates if the alarm is triggered on the voltage drop below the limit, allows to reset alarms.
Value can be found in the published state on the `alarm_voltage_min` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"alarm_voltage_min": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"alarm_voltage_min": NEW_VALUE}`.
If value equals `true` alarm_voltage_min is ON, if `false` OFF.

### Alarm_voltage_max (binary)
Indicates if the alarm is triggered on the voltage rise above the limit, allows to reset alarms.
Value can be found in the published state on the `alarm_voltage_max` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"alarm_voltage_max": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"alarm_voltage_max": NEW_VALUE}`.
If value equals `true` alarm_voltage_max is ON, if `false` OFF.

### Alarm_power_max (binary)
Indicates if the alarm is triggered on the active power rise above the limit, allows to reset alarms.
Value can be found in the published state on the `alarm_power_max` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"alarm_power_max": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"alarm_power_max": NEW_VALUE}`.
If value equals `true` alarm_power_max is ON, if `false` OFF.

### Rssi (numeric)
RSSI seen by the device.
Value can be found in the published state on the `rssi` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `-128` and the maximum value is `127`.
The unit of this value is `dB`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


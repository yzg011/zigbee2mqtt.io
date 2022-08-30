---
title: "TuYa MIR-HE200-TY_fall control via MQTT"
description: "Integrate your TuYa MIR-HE200-TY_fall via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-01-31T17:42:44
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa MIR-HE200-TY_fall

|     |     |
|-----|-----|
| Model | MIR-HE200-TY_fall  |
| Vendor  | TuYa  |
| Description | Human presence sensor with fall function |
| Exposes | illuminance_lux, presence, occupancy, motion_speed, motion_direction, radar_sensitivity, radar_scene, tumble_switch, fall_sensitivity, tumble_alarm_time, fall_down_status, static_dwell_alarm, linkquality |
| Picture | ![TuYa MIR-HE200-TY_fall](https://www.zigbee2mqtt.io/images/devices/MIR-HE200-TY_fall.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Illuminance_lux (numeric)
Measured illuminance in lux.
Value can be found in the published state on the `illuminance_lux` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `lx`.

### Presence (binary)
Indicates whether the device detected presence.
Value can be found in the published state on the `presence` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` presence is ON, if `false` OFF.

### Occupancy (binary)
Indicates whether the device detected occupancy.
Value can be found in the published state on the `occupancy` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` occupancy is ON, if `false` OFF.

### Motion_speed (numeric)
Speed of movement.
Value can be found in the published state on the `motion_speed` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Motion_direction (enum)
direction of movement from the point of view of the radar.
Value can be found in the published state on the `motion_direction` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `standing_still`, `moving_forward`, `moving_backward`.

### Radar_sensitivity (numeric)
sensitivity of the radar.
Value can be found in the published state on the `radar_sensitivity` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"radar_sensitivity": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `10`.

### Radar_scene (enum)
presets for sensitivity for presence and movement.
Value can be found in the published state on the `radar_scene` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"radar_scene": NEW_VALUE}`.
The possible values are: `default`, `area`, `toilet`, `bedroom`, `parlour`, `office`, `hotel`.

### Tumble_switch (enum)
Tumble status switch.
Value can be found in the published state on the `tumble_switch` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"tumble_switch": NEW_VALUE}`.
The possible values are: `ON`, `OFF`.

### Fall_sensitivity (numeric)
fall sensitivity of the radar.
Value can be found in the published state on the `fall_sensitivity` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"fall_sensitivity": NEW_VALUE}`.
The minimal value is `1` and the maximum value is `10`.

### Tumble_alarm_time (numeric)
tumble alarm time.
Value can be found in the published state on the `tumble_alarm_time` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"tumble_alarm_time": NEW_VALUE}`.
The minimal value is `1` and the maximum value is `5`.
The unit of this value is `min`.

### Fall_down_status (enum)
fall down status.
Value can be found in the published state on the `fall_down_status` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `none`, `maybe_fall`, `fall`.

### Static_dwell_alarm (text)
static dwell alarm.
Value can be found in the published state on the `static_dwell_alarm` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


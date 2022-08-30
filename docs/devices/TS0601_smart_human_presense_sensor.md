---
title: "TuYa TS0601_smart_human_presense_sensor control via MQTT"
description: "Integrate your TuYa TS0601_smart_human_presense_sensor via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-04-30T08:00:58
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa TS0601_smart_human_presense_sensor

|     |     |
|-----|-----|
| Model | TS0601_smart_human_presense_sensor  |
| Vendor  | TuYa  |
| Description | Smart Human presence sensor |
| Exposes | illuminance_lux, presence, target_distance, radar_sensitivity, minimum_range, maximum_range, detection_delay, fading_time, self_test, linkquality |
| Picture | ![TuYa TS0601_smart_human_presense_sensor](https://www.zigbee2mqtt.io/images/devices/TS0601_smart_human_presense_sensor.jpg) |


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

### Target_distance (numeric)
Distance to target.
Value can be found in the published state on the `target_distance` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `m`.

### Radar_sensitivity (numeric)
sensitivity of the radar.
Value can be found in the published state on the `radar_sensitivity` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"radar_sensitivity": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `9`.

### Minimum_range (numeric)
Minimum range.
Value can be found in the published state on the `minimum_range` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"minimum_range": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `9.5`.
The unit of this value is `m`.

### Maximum_range (numeric)
Maximum range.
Value can be found in the published state on the `maximum_range` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"maximum_range": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `9.5`.
The unit of this value is `m`.

### Detection_delay (numeric)
Detection delay.
Value can be found in the published state on the `detection_delay` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"detection_delay": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `10`.
The unit of this value is `s`.

### Fading_time (numeric)
Fading time.
Value can be found in the published state on the `fading_time` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"fading_time": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `1500`.
The unit of this value is `s`.

### Self_test (enum)
Self_test, possible resuts: checking, check_success, check_failure, others, comm_fault, radar_fault..
Value can be found in the published state on the `self_test` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `checking`, `check_success`, `check_failure`, `others`, `comm_fault`, `radar_fault`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


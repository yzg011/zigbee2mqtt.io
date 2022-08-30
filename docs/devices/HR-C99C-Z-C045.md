---
title: "ADEO HR-C99C-Z-C045 control via MQTT"
description: "Integrate your ADEO HR-C99C-Z-C045 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2020-12-06T20:18:53Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# ADEO HR-C99C-Z-C045

|     |     |
|-----|-----|
| Model | HR-C99C-Z-C045  |
| Vendor  | ADEO  |
| Description | RGB CTT LEXMAN ENKI remote control |
| Exposes | battery, action, linkquality |
| Picture | ![ADEO HR-C99C-Z-C045](https://www.zigbee2mqtt.io/images/devices/HR-C99C-Z-C045.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
Hold small reset button pressed (located on the backside of remote) for 3
seconds (until the front LED blinks) and device will reset and will attempt to join network.
<!-- Notes END: Do not edit below this line -->


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `simulated_brightness`: Simulate a brightness value. If this device provides a brightness_move_up or brightness_move_down action it is possible to specify the update interval and delta. Example:
```yaml
simulated_brightness:
  delta: 20 # delta per interval, default = 20
  interval: 200 # interval in milliseconds, default = 200
```


## Exposes

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Action (enum)
Triggered action (e.g. a button click).
Value can be found in the published state on the `action` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `on`, `off`, `scene_1`, `scene_2`, `scene_3`, `scene_4`, `color_saturation_step_up`, `color_saturation_step_down`, `color_stop`, `color_hue_step_up`, `color_hue_step_down`, `color_temperature_step_up`, `color_temperature_step_down`, `brightness_step_up`, `brightness_step_down`, `brightness_stop`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


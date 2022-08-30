---
title: "Xiaomi JT-BZ-01AQ/A control via MQTT"
description: "Integrate your Xiaomi JT-BZ-01AQ/A via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-01-31T17:42:44
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Xiaomi JT-BZ-01AQ/A

|     |     |
|-----|-----|
| Model | JT-BZ-01AQ/A  |
| Vendor  | Xiaomi  |
| Description | Aqara smart natural gas detector |
| Exposes | gas, gas_density, gas_sensitivity, selftest, test, mute_buzzer, mute, linkage_alarm, state, power_outage_count, linkquality |
| Picture | ![Xiaomi JT-BZ-01AQ/A](https://www.zigbee2mqtt.io/images/devices/JT-BZ-01AQ-A.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### Adapter firmware
In order for this device to work, at least the following firmware is required on your adapter:
- CC2530/CC2531: [`20211115`](https://github.com/Koenkk/Z-Stack-firmware/tree/Z-Stack_Home_1.2_20211115/20211116/coordinator/Z-Stack_Home_1.2/bin)
- CC1352/CC2652: [`20211114`](https://github.com/Koenkk/Z-Stack-firmware/tree/7c5a6da0c41855d42b5e6506e5e3b496be097ba3/coordinator/Z-Stack_3.x.0/bin)
- CC2538: [`20211222`](https://github.com/jethome-ru/zigbee-firmware/tree/master/ti/coordinator/cc2538_cc2592)
- Conbee II: [`0x26720700`]( http://deconz.dresden-elektronik.de/deconz-firmware/deCONZ_ConBeeII_0x26720700.bin.GCF)

*Note that if you have already paired the device you will need to repair it after upgrading your adapter firmware.*

### Pairing
Quickly press the button three times in a row.
After this the device will automatically join.

![JT-BZ-01AQ/A pairing](../images/pairing/JT-BZ-01AQ_A_pairing.jpg)
<!-- Notes END: Do not edit below this line -->

## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).



## Exposes

### Gas (binary)
Indicates whether the device detected gas.
Value can be found in the published state on the `gas` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"gas": ""}`.
It's not possible to write (`/set`) this value.
If value equals `true` gas is ON, if `false` OFF.

### Gas_density (numeric)
Value of gas concentration.
Value can be found in the published state on the `gas_density` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"gas_density": ""}`.
It's not possible to write (`/set`) this value.
The unit of this value is `%LEL`.

### Gas_sensitivity (enum)
Gas concentration value at which an alarm is triggered ("10%LEL" is more sensitive than "15%LEL").
Value can be found in the published state on the `gas_sensitivity` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"gas_sensitivity": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"gas_sensitivity": NEW_VALUE}`.
The possible values are: `10%LEL`, `15%LEL`.

### Selftest (enum)
Starts the self-test process (checking the indicator light and buzzer work properly).
Value will **not** be published in the state.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"selftest": NEW_VALUE}`.
The possible values are: `Test`.

### Test (binary)
Self-test in progress.
Value can be found in the published state on the `test` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` test is ON, if `false` OFF.

### Mute_buzzer (enum)
Mute the buzzer for 10 minutes (buzzer cannot be pre-muted, because this function only works when the alarm is triggered).
Value will **not** be published in the state.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"mute_buzzer": NEW_VALUE}`.
The possible values are: `Mute`.

### Mute (binary)
Buzzer muted.
Value can be found in the published state on the `mute` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"mute": ""}`.
It's not possible to write (`/set`) this value.
If value equals `true` mute is ON, if `false` OFF.

### Linkage_alarm (binary)
When this option is enabled and a gas leak is detected, other detectors with this option enabled will also sound the alarm buzzer.
Value can be found in the published state on the `linkage_alarm` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"linkage_alarm": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"linkage_alarm": NEW_VALUE}`.
If value equals `true` linkage_alarm is ON, if `false` OFF.

### State (binary)
"Preparation" or "work" (measurement of the gas concentration value and triggering of an alarm are only performed in the "work" state).
Value can be found in the published state on the `state` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.
It's not possible to write (`/set`) this value.
If value equals `preparation` state is ON, if `work` OFF.

### Power_outage_count (numeric)
Number of power outages (since last pairing).
Value can be found in the published state on the `power_outage_count` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"power_outage_count": ""}`.
It's not possible to write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


---
title: "Xiaomi QBCZ15LM control via MQTT"
description: "Integrate your Xiaomi QBCZ15LM via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-09-01T18:11:17Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Xiaomi QBCZ15LM

|     |     |
|-----|-----|
| Model | QBCZ15LM  |
| Vendor  | Xiaomi  |
| Description | Aqara smart wall outlet H1 (USB) |
| Exposes | switch (state), power, energy, device_temperature, voltage, current, power_outage_memory, led_disabled_night, button_lock, button_switch_mode, overload_protection, linkquality |
| Picture | ![Xiaomi QBCZ15LM](https://www.zigbee2mqtt.io/images/devices/QBCZ15LM.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->

## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `device_temperature_precision`: Number of digits after decimal point for device_temperature, takes into effect on next report of device. The value must be a number with a minimum value of `0` and with a with a maximum value of `3`

* `device_temperature_calibration`: Calibrates the device_temperature value (absolute offset), takes into effect on next report of device. The value must be a number.


## Exposes

### Switch (relay endpoint)
The current state of this switch is in the published state under the `state_relay` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_relay": "ON"}`, `{"state_relay": "OFF"}` or `{"state_relay": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_relay": ""}`.

### Switch (usb endpoint)
The current state of this switch is in the published state under the `state_usb` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_usb": "ON"}`, `{"state_usb": "OFF"}` or `{"state_usb": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_usb": ""}`.

### Power (numeric)
Instantaneous measured power.
Value can be found in the published state on the `power` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W`.

### Energy (numeric)
Sum of consumed energy.
Value can be found in the published state on the `energy` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `kWh`.

### Device_temperature (numeric)
Temperature of the device.
Value can be found in the published state on the `device_temperature` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `°C`.

### Voltage (numeric)
Measured electrical potential value.
Value can be found in the published state on the `voltage` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `V`.

### Current (numeric)
Instantaneous measured electrical current.
Value can be found in the published state on the `current` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `A`.

### Power_outage_memory (binary)
Enable/disable the power outage memory, this recovers the on/off mode after power failure.
Value can be found in the published state on the `power_outage_memory` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"power_outage_memory": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"power_outage_memory": NEW_VALUE}`.
If value equals `true` power_outage_memory is ON, if `false` OFF.

### Led_disabled_night (binary)
Enable/disable the LED at night.
Value can be found in the published state on the `led_disabled_night` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"led_disabled_night": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"led_disabled_night": NEW_VALUE}`.
If value equals `true` led_disabled_night is ON, if `false` OFF.

### Button_lock (binary)
Disables the physical switch button.
Value can be found in the published state on the `button_lock` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"button_lock": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"button_lock": NEW_VALUE}`.
If value equals `ON` button_lock is ON, if `OFF` OFF.

### Button_switch_mode (enum)
Control both relay and usb or only the relay with the physical switch button.
Value can be found in the published state on the `button_switch_mode` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"button_switch_mode": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"button_switch_mode": NEW_VALUE}`.
The possible values are: `relay`, `relay_and_usb`.

### Overload_protection (numeric)
Maximum allowed load, turns off if exceeded.
Value can be found in the published state on the `overload_protection` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"overload_protection": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"overload_protection": NEW_VALUE}`.
The minimal value is `100` and the maximum value is `2500`.
The unit of this value is `W`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


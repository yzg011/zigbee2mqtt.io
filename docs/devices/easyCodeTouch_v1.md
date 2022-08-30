---
title: "Onesti Products AS easyCodeTouch_v1 control via MQTT"
description: "Integrate your Onesti Products AS easyCodeTouch_v1 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-10-30T12:58:50
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Onesti Products AS easyCodeTouch_v1

|     |     |
|-----|-----|
| Model | easyCodeTouch_v1  |
| Vendor  | Onesti Products AS  |
| Description | Zigbee module for EasyAccess code touch series |
| Exposes | lock (state, lock_state), battery, sound_volume, action_source_name, action_user, action, auto_relock, pin_code, linkquality |
| Picture | ![Onesti Products AS easyCodeTouch_v1](https://www.zigbee2mqtt.io/images/devices/easyCodeTouch_v1.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Lock 
The current state of this lock is in the published state under the `state` property (value is `LOCK` or `UNLOCK`).
To control this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "LOCK"}` or `{"state": "UNLOCK"}`.
To read the current state of this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.
This lock exposes a lock state which can be found in the published state under the `lock_state` property. It's not possible to read (`/get`) or write (`/set`) this value. The possible values are: `not_fully_locked`, `locked`, `unlocked`.

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Sound_volume (enum)
Sound volume of the lock.
Value can be found in the published state on the `sound_volume` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"sound_volume": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"sound_volume": NEW_VALUE}`.
The possible values are: `silent_mode`, `low_volume`, `high_volume`.

### Action_source_name (enum)
Source of the triggered action on the lock.
Value can be found in the published state on the `action_source_name` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `keypad`, `rfid`, `manual`, `rf`.

### Action_user (numeric)
ID of user that triggered the action on the lock.
Value can be found in the published state on the `action_user` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Action (enum)
Triggered action (e.g. a button click).
Value can be found in the published state on the `action` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `keypad_lock`, `keypad_unlock`, `keypad_unlock`, `manual_lock`, `manual_unlock`, `key_lock`, `key_unlock`, `fingerprint_lock`, `fingerprint_unlock`, `rfid_lock`, `rfid_unlock`, `lock`, `zigbee_unlock`.

### Auto_relock (binary)
Auto relock after 7 seconds..
Value can be found in the published state on the `auto_relock` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"auto_relock": NEW_VALUE}`.
If value equals `true` auto_relock is ON, if `false` OFF.

### Pin_code (composite)
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"pin_code": {"user": VALUE, "user_type": VALUE, "user_enabled": VALUE, "pin_code": VALUE}}`
- `user` (numeric): User ID to set or clear the pincode for. 
- `user_type` (enum): Type of user, unrestricted: owner (default), (year|week)_day_schedule: user has ability to open lock based on specific time period, master: user has ability to both program and operate the door lock, non_access: user is recognized by the lock but does not have the ability to open the lock. Allowed values: `unrestricted`, `year_day_schedule`, `week_day_schedule`, `master`, `non_access`
- `user_enabled` (binary): Whether the user is enabled/disabled. Allowed values: `true` or `false`
- `pin_code` (numeric): Pincode to set, set pincode to null to clear. 

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


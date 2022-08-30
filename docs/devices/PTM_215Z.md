---
title: "EnOcean PTM 215Z control via MQTT"
description: "Integrate your EnOcean PTM 215Z via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-09-02T18:14:38Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# EnOcean PTM 215Z

|     |     |
|-----|-----|
| Model | PTM 215Z  |
| Vendor  | EnOcean  |
| Description | Pushbutton transmitter module |
| Exposes | action, linkquality |
| Picture | ![EnOcean PTM 215Z](https://www.zigbee2mqtt.io/images/devices/PTM-215Z.jpg) |
| White-label | Niko 91004, NodOn CWS-4-1-01_HUE, Vimar 03906 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Green Power
This is a Zigbee Green Power device which allows it to be very energy efficient.
Messages from Green Power devices cannot be "understood" by normal Zigbee devices, therefore they need to be "translated" first.
Not all Zigbee devices can do this translation, currently the only devices known to do this are Philips Hue devices. This means that the Green Power device has to be in range of a Philips Hue device in order to use it.

Green Power devices don't support binding and are not included in network scans.

### Pairing
This device has 4 buttons:

| Number | Button | Position |
|-|-|-|
| 1 | A0 | top left |
| 2 | A1 | bottom left |
| 3 | B0 | top right |
| 4 | B1 | bottom right |

In case the module is integrated in a single rocker switch, you need to remove the caps to expose all buttons. A button can be pressed by holding the contact of that button and then push the energy bar.

To pair it, hold the corresponding button for that channel for 7 seconds or more.

| Button | Channel |
|-|-|
| A0 | 15 |
| A1 | 20 |
| B0 | 11 |
| B1 | 25 |

Once the device is paired you need to confirm the channel. To do this press A1 and B0 together. Important: don't press any other buttons between this and the pairing.

In case you want to pair it to a different channel you have to factory reset the device. This can be done by pressing all buttons (A0, A1, B0 and B1) simultaneously for at least 7 seconds.

Alternatively, you should be able to reset the switch with the following pattern:
1. Press top left (A0)
2. Press and hold top right (B0) for about 10 seconds 
3. press top right (B0) and bottom left (A1) at the same time 
4. press top left (A0)
Note: Please make sure the module is positioned the right way up.
<!-- Notes END: Do not edit below this line -->



## Exposes

### Action (enum)
Triggered action (e.g. a button click).
Value can be found in the published state on the `action` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The possible values are: `press_1`, `release_1`, `press_2`, `release_2`, `press_3`, `release_3`, `press_4`, `release_4`, `press_1_and_3`, `release_1_and_3`, `press_2_and_4`, `release_2_and_4`, `press_energy_bar`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.


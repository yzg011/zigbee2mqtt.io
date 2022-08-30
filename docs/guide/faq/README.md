---
sidebarDepth: 0
---

# FAQ

[[toc]]


## Why does my device not or fail to pair?
This problem can be divided in 2 categories; no logging is shown at all OR interview fails.

### No logging is shown at all
- Make sure [joining is enabled](../usage/pairing_devices.md).
- There can be too much interference, try connecting the coordinator USB through an USB extension cable. This problem occurs a lot when used in combination with a Raspberry Pi 3 and 4.
- If you are using a Raspberry Pi, try disconnecting any other USB devices. If after that pairing works, try connecting the USB devices via a powered USB hub.
- Make sure that any other Zigbee networks/hubs are powered down. When you e.g. want to pair an IKEA bulb which was first paired to the IKEA gateway make sure to power down the IKEA gateway. If that doesn't help also try powering down all devices that are connected to the IKEA hub.
- If it's a battery powered device, try replacing the battery.
- You've hit the device limit of the coordinator, especially occurs when using the CC2531 or CC2530 in combination with the source routing firmware. Try reflashing the coordinator and immediately pair the device after starting Zigbee2MQTT.
- Try pairing the device closer to the coordinator.
- CC2531/CC2530 coordinator only:
  - Stop Zigbee2MQTT, unplug the coordinator, wait 10 seconds, plug the coordinator, start Zigbee2MQTT and try to pair the device again.
  - If none of the above helps, try to reflash the coordinator (does not require repairing of already paired devices).

### Interview fails
- Try pairing the device closer to the coordinator.
- There can be too much interference, try connecting the coordinator USB through an USB extension cable. This problem occurs a lot when used in combination with a Raspberry Pi 4.
- If it’s a battery powered device, try replacing the battery. Try to keep the device awake by pressing the button of the device (if any) every 3 seconds.
- Try repairing the device again for 2 or 3 times.
- This might be a Zigbee2MQTT bug, [Create a new issue](https://github.com/Koenkk/zigbee2mqtt/issues/new) with the zigbee-herdsman debug logging attached to it. [How to enable zigbee-herdsman debug logging](../usage/debug.md#zigbee-herdsman-debug-logging).
- If device joins with `0x000000000000000` as `ieeeAddress` (you will see: `Starting interview of '0x0000000000000000'` in the Zigbee2MQTT log) your CC253X might be broken. [See issue #2761](https://github.com/Koenkk/zigbee2mqtt/issues/2761).
- In case the device is a bulb, try resetting it through [Touchlink](../usage/touchlink.md)
- Try pairing close to a bulb (light) router instead of the coordinator.

## How do I migrate from one adapter to another?
Want to migrate from e.g. a CC2531 to a more powerful adapter (e.g. ZZH)? Then follow these instructions:
1. First make sure you are running the latest version of Zigbee2MQTT
1. Stop Zigbee2MQTT
1. Determine wether migrating [requires repairing of your devices](#what-does-and-does-not-require-repairing-of-all-devices)
    - If repairing is required: remove `data/coordinator_backup.json` (if it exists) and `data/database.db`
    - If repairing is **not** required: [copy the ieee address of the old adpter into the new one](../adapters/flashing/copy_ieeaddr.html)
1. Update the `serial` -> `port`  in your `configuration.yaml`
1. Start Zigbee2MQTT
  - If repairing was required:
      1. Disconnect power of all mains powered devices
      1. Start repairing devices 1 by 1
  - If repairing was **not** required and your devices do not respond; restart some routers by removing them from the mains power for a few seconds.

## How do I move my Zigbee2MQTT instance to a different environment?
Details about your network are stored in both the coordinator and files under the `data/` directory. To move your instance to another environment move the contents of the `data` directory and update the path to your coordinator in your `configuration.yaml`. Now you can start Zigbee2MQTT.

## What does and does not require repairing of all devices?
### Requires repairing
You need to re-pair all you devices when:
- Changing the network key (`network_key`), Zigbee channel (`channel`) or panID (`pan_id`)  in `configuration.yaml`.
- Switching between adapters requires repairing, **except when**:
  - When adapters are the same repairing is **not** required (e.g. CC2531 -> CC2531)
  - Switching from a CC2530 or CC2531 based adapter to a CC2538/CC2652/CC1352 based adapter does **not** require repairing (e.g. CC2531 -> CC2652)
  - Switching between CC2538, CC2652 and CC1352 based adapters does **not** require repairing (e.g. CC2538 -> CC2652)

### Doesn't require repairing
You **don't** need to re-pair your devices when:
- Updating or downgrading Zigbee2MQTT to a different version.
- Updating the coordinator firmware.
  - If after flashing you fail to control your devices it helps to:
    - Wait a few minutes so that the Zigbee network can settle.
    - Send Zigbee commands (e.g. turn on/off) to the device.
    - Reboot the device (unplug and plug power).
- Switching the system running Zigbee2MQTT.
    - When doing this, make sure to copy over the contents of the `data` directory.

## Why are some links missing from my networkmap?
No worry, in case it happens with end devices (battery powered) it most of the times **does not** mean the devices aren't connected to the network map anymore.
Some end devices (e.g. Xiaomi door sensor) sleep for a too long time which causes the parent (router child ageing) to remove it from it from its child table. This is what causes the missing link. Even while its not in the child table anymore, the end device can still communicate via the router. This does not always happen since not all routers use child ageing (this is a Zigbee 3.0 feature).

## Why is the `action` property always empty?
When the Home Assistant integration is enabled (`homeassistant: true` in your `configuration.yaml`) the `action` property of your e.g. buttons will almost always be empty. Whenever an `action` is published e.g. `{"action": "single"}` it will be immediately followed up by a `{"action": ""}`. This is to trigger a state change in the Home Assistant action sensor (so that it can be used in e.g. automations).

## I read that Zigbee2MQTT has a limit of 20 devices (when using a CC2530/CC2531 adapter), is this true?
Definitely not! Example given: the default Zigbee2MQTT CC2531 firmware indeed supports 20 devices connected **directly** to the coordinator. However, by having routers in your network the network size can be extended. Probably all AC powered devices e.g. bulbs serve as a router, you can even use another [CC2530/CC2531 as a router](../../advanced/zigbee/05_create_a_cc2530_router.md) (which has a limit of 21 devices).

### Example
When using the default Zigbee2MQTT CC2531 coordinator firmware + 2 CC2531 routers your device limit will be:
- Coordinator: 15 - 2 routers = 13
- Router 1: 21
- Router 2: 21
- **Device limit of 55 devices**

## Common error codes
A list of common error codes and what to do in case of them:
- `MAC_CHANNEL_ACCESS_FAILURE`: this happens when the wireless spectrum is too occupied. Mostly happens when a microwave is on or when there are WiFi networks on the same channel. See [Reduce Wifi interference by changing the Zigbee channel](../../advanced/zigbee/02_improve_network_range_and_stability.md#reduce-wifi-interference-by-changing-the-zigbee-channel) how to fix this.
- `NWK_TABLE_FULL`: [reported](https://github.com/Koenkk/zigbee2mqtt/issues/4964#issuecomment-757022560) to have same root cause as the above `MAC_CHANNEL_ACCESS_FAILURE`

## How do I run multiple instances of Zigbee2MQTT?
In case you setup multiple instances of Zigbee2MQTT it's important to use a different `base_topic` and `channel`. This can be configured in the [`configuration.yaml`](../configuration/README.md).

## Zigbee2MQTT crashes after some time
If after some uptime Zigbee2MQTT crashes with errors like: `SRSP - AF - dataRequest after 6000ms` or `SRSP - ZDO - mgmtPermitJoinReq after 6000ms` it means the adapter has crashed.
- Normally this can be fixed by replugging the adapter and restarting Zigbee2MQTT
- If you are using a CC2530 or CC2531 adapter consider upgrading to one of the [recommended adapters](../adapters/README.md). The CC2530/CC2531 is considered legacy hardware and runs into memory corruption easily.
- Make sure you are using the latest firmware on your adapter, see the [adapter page](../adapters/README.md) for a link to the latest firmware.
- If using a Raspberry Pi; this problem can occur if you are using a bad power supply or when other USB devices are connected direclty to the Pi (especially occurs with external SSD), try connecting other USB devices through a powered USB hub.
- Disable the USB autosuspend feature, if `cat /sys/module/usbcore/parameters/autosuspend` returns `1` or `2` it is enabled; to disable execute:
```bash
sed -i 's/GRUB_CMDLINE_LINUX_DEFAULT="/&usbcore.autosuspend=-1 /' /etc/default/grub
update-grub
systemctl reboot
```
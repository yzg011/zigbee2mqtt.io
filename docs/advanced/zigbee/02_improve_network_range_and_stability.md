---
---

# Improve network range and stability
In case you are experiencing an unstable or bad network range you can do the following things to improve your network.

## USB based adapter
### Connect the adapter using an USB extension cable
The range of these adapters can greatly be improved when connecting them with an USB extension
cable instead of directly plugging it into the computer (e.g. Raspberry Pi). When plugged directly into the computer, the antenna suffers from interference of radio signals and electrical components of the computer. Also be sure not to position the adapter too close
to any other radio transmitting devices (e.g. a Wi-Fi router) or an SSD. A USB extension cable of 50 cm is already enough to reduce the interference.

**Do not underestimate this!** Placing your adapter close to an USB port can kill the radio signal entirely as demonstrated in [this article](https://www.unit3compliance.co.uk/2-4ghz-intra-system-or-self-platform-interference-demonstration/).

### Try different orientations of the adapter
RF connection between the adapter and other devices also depends on the way it is oriented in space. You might be having very poor `linkquality` reports and intermittent ping failures but once the adapter is rotated a little it all can change greatly without re-locating the coordinator far away. Try to experiment with positioning and orienting the adapter in space while monitoring the `linkquality` values reported. You might find it useful to buy a small rotating USB connector like this:

![rotating USB connector](https://i.imgur.com/AI41Oxz.png)

## Reduce Wi-Fi interference by changing the Zigbee channel
**Changing the Zigbee channel requires repairing of all your devices!**

As Wi-Fi and Zigbee both operate on the same frequency space (2.4 GHz), they can interfere with each other. By using the correct Zigbee channel, interference with Wi-Fi can (partly) be avoided. A good article explaining this is [Zigbee and Wi-Fi Coexistence](https://www.metageek.com/training/resources/zigbee-wifi-coexistence.html).

To change the Zigbee channel Zigbee2MQTT uses you have to set the [`channel` in `configuration.yaml`](../../guide/configuration/zigbee-network.md).

## Interference from other 2.4 GHz devices
Any device using the open 2.4 GHz spectrum could interfere with Zigbee such as Bluetooth or gaming devices like Logitech “Unifying” or “Lightspeed” or Razer “Hyperspeed Wireless”.

## Adding more routers to your network
In a Zigbee network, each router will extend the range of the network ([read more about this](./01_zigbee_network.md)). Almost all AC powered devices will serve as a router.

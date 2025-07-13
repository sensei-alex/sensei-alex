---
runner: none
prev: "[[lab-what-is-a-microcontroller-board]]"
tags:
- resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

## Direct communication over `UART`
Basically everything that has a chip in it can speak `UART`. It's a protocol (a set of rules) that describes how to exchange text messages.

It's used everywhere because it's very simple. To send a message, you just need to encode it in binary and apply current to a wire to send a 1 or remove it to send a 0. Then you can use a second wire receive data in the same manner.

## Wired communication over USB
USB is much more complex than UART, that's why it is not used in every appliance. To exchange data, the devices must first introduce each other, that's not a very easy process.

In exchange for that, you get a lot more capabilities. UART can only do text, USB allows you to build
- internet-connected devices
- displays
- speakers
- microphones
- storage devices
- mice
- keyboards
- macropads
- crazy PCIe things

## Local Network with Wi-Fi
The `wemos s2 mini` has a Wi-Fi controller and a tiny antenna. This allows you to connect it to your router and control it remotely. There are other options available, of course, Bluetooth is often used for remote control. But the main perk that comes with using Wi-Fi is that you can then trivially connect your device to the wider internet, allowing it to be controlled from *anywhere*.

## What are we going to use?
All 3. UART is good for simple controller-to-controller communication, the `wemos` must be programmed over USB the first time, and then we can use Wi-Fi for convenience - it's no fun to build a moving robot that is tethered to your computer by a wire :)
---
runner: none
prev: "[[lab-mcu]]"
next: "[[lab-firmware]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

## Direct communication over `UART`
Basically everything that has a chip in it can speak `UART`. It's a protocol (a set of rules) that describes how to exchange text messages.

It's used everywhere because it's very simple. To send a message, you just need to encode it in binary and apply current to a wire to send a 1 or remove it to send a 0. Then you can use a second wire receive data in the same manner.

## Direct communication over USB
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
- MIDI devices
- etc

## USB-TTL
Some MCUs (like the `ESP32 C3`) don't fully support USB, but still have the USB *connector*. They are actually using UART, but have a built-in converter that translates USB to UART and UART to USB.

This compromise means that
- the chip can be simpler and cheaper (as it doesn't need to implement all of USB's features)
- you can actually plug it directly into your laptop
- but you can't use the interface for anything that is not text

This is also how you would usually connect MCUs that only speak UART. You can get dedicated adapter chips that don't have a microcontroller, they just do the translation.

## Local Network with Wi-Fi
Your board has a Wi-Fi controller and a tiny antenna. This allows you to connect it to your router and control it remotely. There are other options available, of course, Bluetooth is often used for remote control. But the main perk that comes with using Wi-Fi is that you can then trivially connect your device to the wider internet, allowing it to be controlled from *anywhere*.

## What are we going to use?
All of them:
- UART is good for simple controller-to-controller communication
- the board must be programmed over USB-TTL the first time
- then we can use Wi-Fi for convenience - it's not fun to build a moving robot that is tethered to your computer by a wire :)
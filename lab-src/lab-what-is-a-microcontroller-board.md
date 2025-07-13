---
runner: none
prev: "[[lab-thermometer]]"
next: "[[lab-how-to-connect-an-mcu-to-a-computer]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

## What's an MCU?
A `MicroController Unit` is a tiny computer. Their main upside is the low cost, which makes them very useful for things like
- appliances
- chargers
- computer mice
- remotes
- calculators
- toys
- etc.

The main downside is that they are not powerful at all. You can't even plug a monitor into most of them.

## What's a Microcontroller Board?
MCUs are tiny chips, not easy to use or solder. Most of them require additional hardware like a clock or a USB port.

A microcontroller board adds these things to an MCU.

## Which One to Use?
There are hundreds of options available.

Different boards have different features, so it depends on your use-case. My go-tos right now are
- the `RP2040 Zero` (or `Raspberry Pi Pico`) for projects where I don't need Wi-Fi
- and the `Wemos S2 mini` for ones where I do.

These two are available almost anywhere in the world and both of them support any language I want to use with them.

## How to Use Them
1. pick a language (we'll start with CircuitPython because it's easy and quick to develop with)
2. write a program
3. put it on the device
4. return to 2 ~~if~~ when it doesn't work

Putting your program on the device can take 2 forms depending on the language:
1. just copy the code (as with CircuitPython). Languages that support this are called *interpreted* because the chip interprets the code line-by-line, just like you.
2. build, then copy the executable (as with Rust or C++). These are *compiled* languages, they use a program on your computer to translate human-readable code into machine-readable ones and zeroes and then the device executes those.
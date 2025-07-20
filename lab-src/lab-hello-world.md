---
prev: "[[lab-firmware]]"
next: "[[lab-libraries]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

The first program people typically write is one that outputs the sentence "Hello, world!" as text to the screen. This is a simple way to test that everything is working correctly.

Please unplug the microcontroller board from your computer and plug it into a phone charger. This will help us test that Wi-Fi is working correctly.

Your browser prevents websites from connecting to your devices wirelessly as the communication between them and the site is unencrypted. This doesn't matter for our purposes since I'm not collecting or storing your data, so there's nothing that really needs encryption.

Go to site settings and allow insecure content like so:
![[scan-security.svg]]

Reload this page. Assuming the board is plugged in, this site will connect to it. This might take about a minute. Then the top right section should load the program from it. The hello world program is baked into circuitpython, so you see it after installing it.

Let's break down the program: `print` is a function. A function is just a command that runs some block of code that's written elsewhere.

The brackets make it actually run, and the `"Hello, world!"` in quotes is the text that it's supposed to do something with.

Type `:w` to re-run a program. This is a shorthand for `:write`, the code editor command that writes (saves) the file. Circuitpython automatically runs files when they are saved.
---
runner: none
prev: "[[lab-connect]]"
next: "[[lab-hello-world]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

You can't just use circuitpython on most MCUs out of the box, you first have to install it (flash it):

- plug the microcontroller board into your computer via `USB`
- make sure you're not using firefox or safari and you are on a computer, not a tablet
- go to https://circuitpython.org/downloads
- type `c3` and click on the first result
- in the card labelled CircuitPython 9.something click "Open Installer"
- select "Full CircuitPython 9.something Install" and follow the instructions. When it prompts you for the password, set it to `hunter2`

Next, you need to configure Wi-Fi.
- [make sure](https://duck.com/how to check if my network is 2.4g) that your home router's network is 2.4GHz
- unplug the board and plug it back in
- navigate to https://code.circuitpython.org/
- click `USB`, then "Connect to Device" and select the one you chose during installation
- look under the "Disconnect" button in the top right corner. If you see "🐍 192.168.something.something", everything's set! Skip the rest of this page
- click "Open" in the top left corner
- select `settings.toml`
- make sure the file is empty
- type `CIRCUITPY_WIFI_SSID="`, then the name of your Wi-Fi router, then `"` and press enter
- type `CIRCUITPY_WIFI_PASSWORD="` and enter your Wi-Fi password, then `"`
- type `CIRCUITPY_WEB_API_PASSWORD="hunter2`. This is the password used by `lab` (this app)
- save the file
- click "Restart" in the top right and wait for it to output a bunch of numbers like `192.168........`. If it doesn't, make sure that you're using a 2.4GHz network and have typed the network name and password correctly.
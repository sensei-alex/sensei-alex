---
prev: "[[lab-looping]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

A relay is an electromechanical device that acts like a switch: it allows the microcontroller to control a high-voltage load using its low-voltage output pins.

Disconnect your MCU board. Turn it upside down and find a pin labelled `5V`, `VBUS` or `VCC`. This is the positive contact. The one labelled `GND` or just `G` is the negative one (the ground).

If your board came without any pins pre-installed, or you don't have a breadboard, you'll need [to solder](https://duck.com/how%20to%20solder%20ifixit) the wires in the next step. If you do have a breadboard and don't know how it works, [read about it](https://duck.com/how%20does%20a%20breadboard%20work).

Connect:
- MCU `5V` to relay `VCC` or `5V`
- MCU `GND` to relay `GND`
- relay `IN1` to any pin on the board that has a number next to it (except 9), just remember that number
- relay `IN2` to any other pin with a number

Power up the board and reload this page. When the code finishes loading:
- go to line 5 by pressing `5G`
- jump to the end of the line using `$`
- press `b` to go to the previous word (`back a word`)
- change it (`cw`) to `IO` followed by the number of the pin you've connected the relay to (like `IO7`)
- save the file and now the relay should be blinking.

You can change the number you give `time.sleep` to be more practical (you wouldn't want to water a plant every second, right?)

Another example of what you could do is `sleep(60 * 60 * 2)`. This will wait for 2 hours. Note that the accuracy of these time measurements is not perfect and can depend on your board.

Congratulations, the relay timer is complete!

---

```python
import time
import board
import digitalio

led = digitalio.DigitalInOut(board.IO7)
led.direction = digitalio.Direction.OUTPUT

while True:
  led.value = False
  time.sleep(60)
  led.value = True
  time.sleep(24 * 60 * 60 - 60)
```
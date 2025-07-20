---
prev: "[[lab-digitalio]]"
next: "[[lab-relays]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

To make the LED blink more than once you could copy the last two lines a bunch of times and alternate between `led.value = True` and `led.value = False`...

Or you could tell the microcontroller to do that for you.

A `while (condition):` loop runs until its *condition* is `True`. That means that `while True:` runs forever.

Go to the end of the file, then line up using `k`. Insert a line above (`O`) and type `while True:`. Return to normal mode and go down a line using `j`. Press `v` to select text (`visual mode`), `j` to select down, and `>` to shift the code right. The shifted code is considered to be inside the loop. This is important. It's also good for readability: you can instantly tell if the code is inside something without even reading it. Save the file and the LED will be on forever.

But we wanted it to blink, right? Can you make it blink? If you're unsure how, press the question mark icon in the bottom left corner.

---

```python
import time
import board
import digitalio

led = digitalio.DigitalInOut(board.LED)
led.direction = digitalio.Direction.OUTPUT
print(led.value)
while True:
  led.value = False
  time.sleep(1)
  led.value = True
  time.sleep(1)
```
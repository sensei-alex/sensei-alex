---
prev: "[[lab-hello-world]]"
next: "[[lab-digitalio]]"
tags:
  - resource
area: "[[lab]]"
publish: "[[lab-src]]"
---

A library (sometimes called a module) is just multple functions doing similar things wrapped in a file. There are libraries for pretty much everything. Some allow you to send electric signals to the contacts of your microcontroller, others help you build servers, apps and bots.

Circuitpython has a lot of useful libraries built in, but you can also install external ones.

To use a library, you first have to import it. They are not imported by default mostly to save memory.

`board` is a built-in module that stores the names of every controllable pin (contact) on the microcontroller board.

Let's ask the microcontroller what pin the LED is connected to:
- delete the current program by typing `dd` (`d` stands for delete and `dd` means to delete a line)
- press `i` to tell the editor that you want to type (`insert`) characters
- type `import board` and press Enter twice
- type `print(board.LED)` (`LED` must be in all capital letters)
- press ESC to tell the editor that you want to enter a command now
- type `:w` to save & run

---

```python
import board

print(board.LED)
```
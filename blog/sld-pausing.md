---
tags:
- resource
area: "[[sld]]"
publish: "[[blog]]"
created: 2025-07-30
updated: 2025-07-30
---

Hello world. A week ago I learned about typst.

In theory, typst is just a typesetting system that makes writing essays and reports easier. I, however, found out about it from https://sdr-podcast.com/episodes/typst-is-pretty-neat where James used it to make a presentation and a simple static UI for an e-ink display (something that I would've done with an SVG). SVGs, are a pain when it comes to working with text, though.

Typst is capable of doing everything [[sld]] did, except it requires the user to code instead of having a graphical UI. Now *I* prefer to code, but I made [[sld]] for a professor at my university, and they don't know how to code.

I still want to use it in place of [[sld]]'s current `Canvas` component because of the extended capabilities it gives me.

Another benefit to using typst for [[sld]] is that I no longer have to deal with different aspect ratios as the user can define the target screen size.

Then I found out that the typst compiler runs in webassembly, took the typst.ts single-file demo and modified it to draw a rectangle from the top left corner to the current coordinates of the mouse. The preview was updating instantly as I moved the mouse around. Instantly! So typst can be a UI engine.

So I thought that maybe it's possible to make a whole visual editor on top of typst, but that'd have nothing in common with the original [[sld]] codebase. I want to work on that (at least for now), so I'm pausing [[sld]].
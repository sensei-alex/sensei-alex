---
tags:
- resource
area: "[[blog]]"
created: 2025-06-09
updated: 2025-06-09
---

Hello world. When I was testing [[lab]] with my friends, they had problems finding the microcontroller board on their LAN. I've decided to look for a way to scan a network from the browser so they don't have to.

Turns out it's not that easy. Avahi exists and does (mostly) what I needed, but it requires a daemon to be installed on the user's system, which I cannot guarantee. I can't just ask the router who's connected either, I don't have the credentials. The dumbest solution that turned out to be the right one was to make a bunch of requests to all possible ip addresses and then keep the ones that responded. This works with circuitpython boards since they have an HTTP server on port 80 that is not blocking access from the local network.

I wrote a little script to test the idea, then decided I may need it later, and now it's a separate project. I've decided to keep it small and trivial just like [[qrs]]. You can check it out over at snlx.net/scan.

The only problem is, as is usual, HTTPS. The browser does not allow me to make an HTTP request from my HTTPS site. I'll think about that tomorrow. See you then!

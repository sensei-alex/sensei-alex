---
tags:
- resource
area: "[[blog]]"
created: 2025-06-10
updated: 2025-06-10
---

Hello world. Like I've mentioned yesterday, [[scan]]'s live demo can't fetch anything from the user's local network because of HTTPS.

The first thing explored to fix that was making the whole site HTTP. This comes basically without risk because I don't collect user info, so there's nothing to intercept. However, I'm pretty sure Certbot is going to break my NGINX config some day if I make one route HTTP and the rest HTTPS.

My next thought was to use `window.open()` to create a new tab and then run the JS there. Unfortunately, that new window still counts as HTTPS. I learned about the `postMessage` API though.

Okay, what if I open a new tab via a data URI? Since it's a data URI, it can't be HTTP, right? Right?
```
Mixed Content: The page at '<URL> html>(cut)</html>' was loaded over HTTPS, but requested an insecure resource '<URL>'. This request has been blocked; the content must be served over HTTPS.
```

Then I tried changing the CSP. That helped, but then I ran into CORS.

As far as I know, there are 2 solutions to my problem:
1. educate the user. Tell them why this is happens and what they need to do to allow it
2. make a downloadable page

I've been doing the latter with both [[lab]] and [[scan]], but the former is obviously the right solution. I'll be switching to that now.

Thinking about it, this is kind of even better because that way any interaction with the local network requires user consent.

If you find a better solution, please let me know though!
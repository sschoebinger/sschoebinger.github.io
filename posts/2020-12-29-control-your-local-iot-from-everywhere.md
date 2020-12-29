---
pageTitle: Control your local iot from everywhere
description: Describes two approaches how to control your local node red installation from the internet (cheep and secure)
---

_The aim of this blog post is to describe two approaches how to control your local node red installation from the internet (cheep and secure). I'll not describe all the details, most of the parts are already described by others and google will help you find the right tutorials. If you need some hints or if you have a question about my iot setup you can contact me on [twitter](https://twitter.com/sschoebi)._

<img src="/img/2020-12-29-iot-from-everywhere.png" alt="control your local iot from everywhere" style="width: 100%;" loading="lazy">
<br/>
<br/>
<br/>

A few months back when we moved to another house there was this garage door which was already electric powered but not connected. I had to use the dedicated remote control to open and close it. Especially when I return with my son and the two dogs I often thought "please let me just say: Siri open/close the garage".

**This was the time when I had the first iot use case that was useful.**

Building that iot use case was fairly simple, I used a [shelly 1](https://shelly.cloud/products/shelly-1-smart-home-automation-relay/) to control the garage door operator, connected that shelly to a mqtt broker installed on a raspberry pi 4 in my local network and installed node red on the raspberry pi to define the iot logic.

One thing which was first not trivial: **how can I control this node red installation from remote?** Without having a public ip address representing the raspberry pi (which I don't want due to security concerns).

The first and simplest solution was using a telegram bot. There is already a [node red plugin](https://flows.nodered.org/node/node-red-contrib-telegrambot) that can be used and there are already tutorials out there how to configure it. I use that bot to remind me to close the garage door after 9 p.m. if it is still open. But for daily usage voice control is much more convenient than writing to a bot.

But unfortunately (at that time) it was not possible to create Siri shortcuts that interact with telegram (bots). **So I needed a generic solution that allowed me to create my Siri shortcut.**

After some investigation [google pub sub](https://cloud.google.com/pubsub/docs/overview) or [pusher](https://pusher.com/) seemed to be a good solution for my problem. It is fully managed, cheep (if you don't have a lot of messages) and node red can connect to it.

The final solution to get my "Siri please open the garage" shortcut is, a function hosted on [vercel](https://vercel.com/dashboard) which gets an API key and the command (open or close).

`https://host.com/myfunction?apikey=<thekey>&command=open`

This function can be called by a static url which can be used in the Siri shortcut. The function forwards the command into google pub sub where it gets consumed by my local node red installation which can trigger the appropriate action to open or close the garage door.

<br/>

The price of this setup is:

- you have to pay for the electricity consumed by the raspberry pi
- the function on vercel is for free
- google pub sub costs $0.01 per month (pusher has a complete free tier)

<br/>
This is an overview of my current setup:
<br/>
<br/>
<img src="/img/2020-12-29-node-red-diagram.png" alt="my iot setup" style="width: 100%;" loading="lazy">

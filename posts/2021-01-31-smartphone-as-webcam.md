---
pageTitle: How to turn your smartphone into a webcam
description: A description of how I turned my broken smartphone into a better webcam
eleventyExcludeFromCollections: false
---

For my daily work I use a macbook pro from 2017, I never liked the video of that webcam (and thats almost the same for all laptops). But as I doesn't use it a lot I never bought a separate webcam. When I was asked last week to give a remote presentation, a [video](https://www.youtube.com/watch?v=x_lHk9Lf-ow) from [Scott Hanselman](https://www.youtube.com/channel/UCL-fHOdarou-CR2XUmK48Og) came to my mind which is about turning your DSLR into a webcam. I first though I'll do the same but unfortunately my Sony DSC-HX50V doesn't have a clean HDMI video signal so it was not possible to follow that way.

However there was my old smartphone (HTC U11) which has a good camera but a broken display. Turning this smartphone into a webcam would be a cheap and good solution. As to my surprise it was pretty easy to do that.

All you need is

1. [Iriun](https://iriun.com/) installed on your mac or windows laptop
1. [Iriun](https://iriun.com/) installed on your smartphone
1. Developer options enabled on your smartphone
1. Your smartphone connected via USB to your laptop

If you open both the Iriun app on your smartphone and the Iriun program on your laptop you'll get a video preview from your phones camera on your laptop. And as it is connected via USB the latency is very good (at least in my setup with Android and MacOS).

<br/>
<img src="/img/2021-01-31-iriun.jpg" alt="iriun on smartphone and laptop" style="width: 100%;" loading="lazy">
<br/>

A first test with [OBS](https://obsproject.com/) worked fine but as I wanted to use this new video source for my presentation in Microsoft Teams I had to follow [these instructions](https://answers.microsoft.com/en-us/msteams/forum/msteams_tfb-msteams_tfmac/microsoft-teams-mac-os-client-is-not-recognizing/d9e863be-d9a4-4d03-a4b8-1b5c7df58828). By default Microsoft Teams on MacOS is not allowed to use that virtual video source from [Iriun](https://iriun.com/). I hope Apple or Iriun will solve that issue soon!

This setup allowed me to reuse my broken smartphone as my webcam which has a much better camera than the laptop internal webcam. In addition I can chose much better perspectives than this standard "face from below" perspective. And last but not least I liked that by connecting the smartphone via USB the video latency is pretty good.

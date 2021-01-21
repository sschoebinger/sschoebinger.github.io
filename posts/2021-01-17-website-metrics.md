---
pageTitle: Website metrics without tracking the user
description: how to get basic website metrics without using google analytics
eleventyExcludeFromCollections: false
---

During Christmas holidays I started this blog and wrote a few articles in the following weeks. I decided to host my blog with [github pages](https://pages.github.com/) and after some time I started asking myself, does anyone read that what I write? Unfortunately [github pages](https://pages.github.com/) doesn't provide any metrics about the usage of my website which forced me to add some js analytics snippet or I had to host my website somewhere else. As I don't wanted to move away from [github pages](https://pages.github.com/) the first thing that came to my mind was adding **google analytics**.

But as an user I don't like, that I'm being tracked all over the web by a few companies and I didn't like the idea of adding the same tracker to my website.

After a short search I found [plausible](https://plausible.io/) which says about itself it is simple, hosted in the EU, 100% self-funded and independent - thats great! Fortunately it has a free trail period of one month which I used to test it. Afterwards it costs $6 per month for up to 10k monthly page views. That feels expensive for basic website metrics of a personal noncommercial website.

**10k page views is that much?** One of my blog posts got a few retweets on twitter, nothing special but it produced about 1k page views in 24h. It is very likely that the 10k plan is enough for my blog but if you get more retweets, a good rank at google or hit the first page of hacker news it is very likely that the 10k plan is not enough anymore. But even if it never exceed the 10k page views because you write only one blog post each one or two months you still have to pay $6 per month to see your ~1k monthly page views.

<img src="/img/2021-01-17-plausible-overview.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">
<br/>
<img src="/img/2021-01-17-plausible-details1.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">
<br/>
<img src="/img/2021-01-17-plausible-details2.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">

<br/>

What a dilemma, [plausible](https://plausible.io/) is a great product but it has [no pricing tier](https://plausible.io/#pricing) that fits the needs of a small personal noncommercial website. I decided to try another alternative to **google analytics** which is [cloudflare web analytics](https://www.cloudflare.com/web-analytics/). It also doesn't track the user and it is for free, what a great fit. I gave it a try and it does the job, I get the basic usage metrics for my website without having additional costs, no tracking of single users, no cookies and so on.

<img src="/img/2021-01-17-cloudflare-overview.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">
<br/>
<img src="/img/2021-01-17-cloudflare-country.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">
<br/>
<img src="/img/2021-01-17-cloudflare-details.png" alt="structure of my site with 11ty" style="width: 100%;" loading="lazy">

<br/>

_Finally [github pages](https://pages.github.com/) for hosting my website and [cloudflare web analytics](https://www.cloudflare.com/web-analytics/) for getting basic insights about the usage of my website is a very good combination that is affordable and protects the users privacy._

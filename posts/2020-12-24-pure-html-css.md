---
pageTitle: pure HTML/CSS webpage that lasts long
---

I read a few times during the last days that creating a web page with **only HTML and CSS**, has the advantage of not being forced to update your frameworks again and again. It is a must for all my side projects that the effort for maintenance is as low as possible (otherwise they get outdated and die).

I started with [john-doe.neocities.org]("https://john-doe.neocities.org/) as a reference and changed a few things (mostly colors). I added my content and deployed the site by using github pages, which was really easy. See my git repo for all details [sschoebinger.github.io](https://github.com/sschoebinger/sschoebinger.github.io/tree/36995863bcb29a2ee526545c4217249136165d34)

<br/>

<blockquote class="twitter-tweet">
  <p lang="en" dir="ltr">
    Steren wrote about something I’ve been meaning to for years. My blog is the
    same, HTML, CSS, and a wee bit of JavaScript only when absolutely necessary.
    <a href="https://t.co/Zr9JJ4nvK2">https://t.co/Zr9JJ4nvK2</a>
  </p>
  &mdash; Seth Vargo (@sethvargo)
  <a
    href="https://twitter.com/sethvargo/status/1341883882786992131?ref_src=twsrc%5Etfw"
    >December 23, 2020</a
  >
</blockquote>
<script
  async
  src="https://platform.twitter.com/widgets.js"
  charset="utf-8"
></script>
<br/>

It was okay to set all this up (with basic HTML and CSS knowledge) and it has some advantages for sure:

- 100% control of designed and structure
- fast (lighthouse 100% on first try)
- easy to deploy (e.g. github pages without CI/CD)
- you learn the basic again

<br/>

<img src="/img/2020-12-24-lighthouse.png" alt="lighthouse 100%" style="width: 60%;">

<br/>

But even with my few pages I already had the wish to **separate my content into different files** and if you start with multiple files you definitely need _templating_. In addition I always like to write content in _markdown_ which is no mandatory feature but nice to have.

**I'll definitely test some of the static site generators and see what is the cost for having templating and markdown support.**

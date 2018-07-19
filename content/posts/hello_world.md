---
title: "Hello World!"
description: Well... Here I am!
tags: [
    "introduction",
]
date: 2018-07-22T00:00:00+02:00
---

So... I finally decided to set up a personal blog. It's powered by [Hugo] which
I had experimented with for quiet a while now. I also played around with some
more advanced publishing platforms like [Ghost] but came to the conclusion that
Hugo is more flexible.

I actually hate writing stuff down, especially for some kind of blog or platform
on the internet and I'm not a good writer anyways. I rather not have my wise
words available to the public eye. So why does this blog even exist?

![knowledge meme][knowledge_meme]
© [makeameme.org][makeameme]

How often have you had a *Déjà-vu* where you wished you had written down some
notes on that particular problem? To be honest, this happens to me on a regular
basis. So this blog only exists to document important knowledge I acquire on
my daily journeys. But the neat side effect of this website being public is that
this knowledge is also available to everybody on the internet. So in the near
future, there might be some content here, which might actually support people.

If you feel the need to contact me about something I have published here, do it!

***

## Tech stack

Some information on how this site is build and hosted:

* This site is powered by [Hugo]
* The theme is forked from the [Cactus Plus Theme], modified and released as
  [Cactus Plus Plus]
* The sources for this site are publicly availabe [on GitHub][site_repo]
* The site is hosted on AWS in an S3 bucket behind CloudFront (AWS CDN)
* [Travis-CI][travis] builds and deploys the site
  * The cron feature is enabled. Building of the site happens every 24 hours.
    This is used to publish posts with a date in the future which has not been
    reached yet and requires no human interaction
  * After deployment to S3 Travis CI invalidates the CloudFront cache to make
    sure the previously deployed files are served correctly

<!-- Links -->
[Cactus Plus Theme]: https://github.com/nodejh/hugo-theme-cactus-plus
[Cactus Plus Plus]: https://github.com/lukasmalkmus/hugo-theme-cactus-plus-plus
[Ghost]: https://ghost.org/
[Hugo]: https://gohugo.io/
[knowledge_meme]: https://media.makeameme.org/created/knowledge-bm3yvd.jpg
[makeameme]: https://makeameme.org/
[site_repo]: https://github.com/lukasmalkmus/hugo-theme-cactus-plus-plus
[travis]: https://travis-ci.com/
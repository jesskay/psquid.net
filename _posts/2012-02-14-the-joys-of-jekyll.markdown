---
layout: post
title: The Joys of Jekyll
tags:
- git
- github
- jekyll
- static
---

Time to dust off the old blog-o-phone again, I think.

A little while ago, I [moved my blog to a blogging engine of my own design and
creation][1]. And all was well and good. But after a while, I started to find
little things I didn't like my original solution to, and gradually the entire
codebase devolved into a functioning, but crufty, relic. And I spent _far_ more
time working on the engine than actually writing any posts, which is toxic for
a blog, especially since 90% of code changes won't result in any obvious visual
changes.

So I started looking around for a solution that didn't need me to maintain the
engine itself, but still had the features I wanted - namely:

 * Markdown (or Textile in a pinch, though I still prefer Markdown)
 * Complete control over page layout.
 * Version controllable
 * Ability to serve it from my own server a plus, but not a requirement

After a little searching, and with a strong recommendation from [moggers87][2],
I settled on [Jekyll][3]. It satisfies the first two requirements _easily_, and
the third and fourth were satisfied together by my decision to use [Github
Pages][4] to host it (another nice result of that is that you can [see the
source of any post exactly as I wrote it][5]). Since the output is just HTML
and CSS, I _could_ also have hosted it on my server, but I was going to use git
to track it anyway, so choosing [Pages][4] killed two birds with one stone.

The much more relaxed visual style was born out of my growing distaste for the
old yellow/black colour-scheme, and my desire to keep the style as simple as
possible this time round.

To sum things up: just from having imported my old posts (mostly
copy-and-paste, since they were already in Markdown on my old engine), and now
from having written this post, I can safely say that (as the title may well
have already told you), Jekyll is an absolute _joy_ to use. If you haven't
tried it, I really can't recommend enough that you go and do so right away!

PSquid out.


[1]: http://psquid.net/2011/06/22/ink-n-mustard/
[2]: http://moggers87.co.uk/
[3]: http://github.com/mojombo/jekyll/
[4]: http://pages.github.com/
[5]: https://github.com/psquid/psquid.github.com

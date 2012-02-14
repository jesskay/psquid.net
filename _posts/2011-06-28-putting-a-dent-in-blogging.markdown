---
layout: post
title: Putting a dent in blogging
tags:
- pun
- terrible pun
- status.net
---

**EDIT**: Since this version of the post is on a github-hosted site, there are
no comments, so the post below is factually incorrect (for this version,
anyway).

What really makes a blog (besides the posts, obviously) is probably the
comments.

The trouble is, if you have to sign up for a blog to comment, that immediately
lowers the chance that you'll actually do so. But go too far the other way, and
you open yourself up to waves of spam from opportunistic spam bots.

Luckily, there's a third way; require an account, but _not one that is unique
to a single blog_. Several of the big blogging engines do it, with ways of
having a global account that works for all blogs using that engine. Then
there's generic authentication providers, OpenID et al, which can be used in a
similar way.

And then, there's what I've now done with this blog: status.net comments. Since
I intend to broadcast "new blog post" messages on identi.ca anyway, it's not
too difficult to harvest replies to that dent, and present them as comments,
just the same as the built-in comments. Maybe I'm not the first to do it, but
I'm proud of my solution, especially since its reuse of my existing statusnet
module allows it to be used with just about any status.net instance.

Anyway, it's switched on as of this post, so barring any catastrophic failures
I couldn't get to occur in testing, it should now be live. Enjoy!

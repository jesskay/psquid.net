---
layout: post
title: OpenID and Status.net
tags:
- openid
- status.net
---

Today I discovered something cool about status.net, that I hadn't known before. Namely, that you can delegate your [OpenID][1] to it. I already had an OpenID identity referenced in my site, but it delegated to Google, which had two problems:

 - It wasn't linked to any one account, so services I logged into would tend get confused if I was logged into a different Google account.
 - It would often forget I was logged in, even if other Google services stayed logged in just fine.

Luckily, it turns out that not only can a status.net profile (such as [mine][2]) be used as the OpenID endpoint I delegate to, but the markup necessary is already present in the profile source itself, so you don't even have to remember the little details of the syntax.

The markup you're looking for are the two `<link>`s with `"openid.*"` `rel` fields (there are also some openid2 fields in there, but those are largely irrelevant for the purposes of this post), so in my case that would be these two lines:

     <link rel="openid.server" href="http://micro.fragdev.com/main/openidserver" />
     <link rel="openid.delegate" href="http://micro.fragdev.com/psquid" />

You can, of course, also just modify those directly to match your instance URL and username, if you don't even want to open up your profile's source.

With those replicated in the `<head>` section of this site's pages, I simply provide "psquid.net" as my OpenID when a site asks for it, confirm the login with Fragdev if I've never used that site before, and then all is good. No random profiles, no unexplained logouts. It just works exactly how it should.


[1]: https://openid.net/
[2]: http://micro.fragdev.com/psquid

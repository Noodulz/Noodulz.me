---
title: Natas3
date: 2020-07-22 21:33:00 -04:00
permalink: "/writeups/OverTheWire/Natas/natas3"
layout: post
---

## There is nothing on this page
<br/>

When inspecting the source, there is a comment leaving a vague hint:
<br/>
*No more information leaks!! Not even Google will find it this time...
<br/>
My first instinct was this must be a `robots.txt` challenge, as it typically bars users from certain webpages. Inputting it into the URL, it leads us to a page with:
</br>
User-agent: *
Disallow: /s3cr3t/
<br/>

And when appending /s3cr3t to the end of the URL, the password is revealed in users.txt 
<br/>
natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
<br/>
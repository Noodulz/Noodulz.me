---
title: Natas1
date: 2020-07-22 21:18:00 -04:00
permalink: "/writeups/OverTheWire/Natas/natas1"
layout: post
---

```
You can find the password for the next level on this page, but rightclicking has been blocked!
```
There are multiple ways to go about checking the source without rightclicking. One particular way is to save the webpage and open it up in a text editor or IDE, either by `CTRL+s` or clicking on settings and pressing "Save Webpage" in your browser. Once doing so, opening the page up in an editor should reveal the password at the bottom.

```
<div id="content">
You can find the password for the
next level on this page, but rightclicking has been blocked!

<!--The password for natas2 is ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi -->
</div>
```
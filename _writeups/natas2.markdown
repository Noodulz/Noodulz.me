---
title: Natas2
date: 2020-07-22 21:28:00 -04:00
permalink: "/writeups/OverTheWire/Natas/natas2"
layout: post
---

`There is nothing on this page `

Checking the source first, there literally is nothing to show. Or so it seems. If you look at the source of the image closely, it indicates that the source lies at `files/pixel.png`, which means there's an accessible directory called `files` on the page. When appending `/files` to the end of the URL, it leads us to a page with a parent directory, with files `pixel.png` and `users.txt`. Obviously, the password must lie in `users.txt`. Clicking the file, it shows a list of usernames and passwords and there goes natas3. 

```
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```
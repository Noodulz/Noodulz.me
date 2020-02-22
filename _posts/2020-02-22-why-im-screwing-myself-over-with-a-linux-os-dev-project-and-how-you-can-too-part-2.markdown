---
title: Why I'm Screwing Myself Over with a Linux OS Dev Project and How You Can Too!
  (part 2)
date: 2020-02-22 01:25:00 -05:00
---

Some of my friends have often joked or chastised me for pursuing compiling my own Linux OS with the [Linux From Scratch](http://www.linuxfromscratch.org) framework. "Why not use Gentoo?", "I use Arch", "Why?". And when the audience at a talk I was at the other day stayed silent to a "Who wants to hear a Linux from Scratch talk huh?", I laughed it off but felt awkward on the inside. Maybe this isn't the right project for me to do. Maybe it may be worthless to others. To most I know who's knee deep in the realm of cybersecurity and binary exploitation anyway, it's the butt of the joke. 

But I am undeterred. So far though it's been a tedious project, I've learned a lot more about Git, workflows, the wonders of Docker containers, and most important of all how a Linux system works and is built. I'm working right now on [Hardened Linux from Scratch](http://www.linuxfromscratch.org/hlfs/view/development/index.html) which teaches you how to build a secure and robust Linux system with up-to-date packages and setting up networking infrastructures and firewalls. I'm on my way to setting up the build packages and then fully building and running the Dockerfile of the entire system to finish. It's been a rather annoying but worthwhile journey, and I can't wait to finally see the finished product. I hope with having built an OS in a Docker container and having it [boot to a GUI](https://github.com/mviereck/x11docker) with the X Windows manager and everything, that my friends and peers will reconsider their blunt remarks. Or at least be wowed. But that's not the point of doing this project. 

Also, I learned that this may not be the most usable OS in the end since to update I'd have to probably rebuild the entire system over and over each release. But perhaps there's another way to make that more efficient. I still have a ways to go, after all. 
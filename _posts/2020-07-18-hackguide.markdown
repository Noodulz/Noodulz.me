---
title: My Personal Structured Study Guide For Delving into Hacking
date: 2020-07-18 19:34:00 -04:00
permalink: "/_posts/hackguide"
layout: post
---

Lately I've spent this summer aimlessly flipping through PDFs of guides on programming and exploitation as well as diving into (what is probably my 5th time) CS50 to revisit the basics and learn the foundation needed to break into this mysterious field. After watching countless videos and reading hundreds of articles every night, though, I find myself getting distracted and off track jumping from resource to resource and book to article, barely getting anywhere. 
<br/>
So after all that time spent, here I'll lay out a structured guide of resources and websites to keep me on track to where I need to be to get to a point of understanding CTFs and overall application security better. Hopefully it may reach some of you guys who may also be bitterly prone to distractions and hopping from guide to guide. 
<br/>
## Level 1
* Even if you're a seasoned hacker or expert in CS, or whether you're a fledgling beginner, there's no better way to start off learning the basics than with [Harvard's CS50](https://www.edx.org/course/cs50s-introduction-to-computer-science). For the 2020 version at least, it'll get you deep into C programming, data structures and algorithms, concepts of memory and pointers (which is also great for understanding buffer overflows later on), Python, SQL, and application development. Basically the foundation of almost everything you'd learn in a 4-year Computer Science program. 
* [Hacking: The Art of Exploitation](https://nostarch.com/hacking2.htm), which is also a great guide in exploring C, Assembly, networking concepts, exploitation and more for a beginner. Most likely after going through this, you'll have enough of a foundation to begin plowing through simple boxes in Hack The Box or easy pwn challenges and work your way up from there. 
* [OverTheWire](https://overthewire.org/wargames/), especially the Bandit and Natas through Krypton down the list are useful ongoing wargames to learn more about Linux and web security and exploitation through hands-on experience and useful hints should you get stuck. 
* [HackSplaining](https://www.hacksplaining.com/lessons), a visual look at common vulnerabilities in web applications.
* [Optional reading, but Code by Charles Petzold is also another good intro to how computers work and why to understand internals better for absolute beginners.](https://www.amazon.com/Code-Language-Computer-Hardware-Software/dp/0735611319)
<br/>
## Level 2
* [TryHackMe's Zero to Hero Boxes Guide](https://blog.tryhackme.com/going-from-zero-to-hero/). There's a map for free members who can't or won't get the subscription, and a map for subscribed members. Personally I find this a much easier and similar alternative to HackTheBox, due to the numerous threads and hints and explanations in each of the boxes to help you understand concepts better. Though, it's best to keep practicing the concepts and exercises taught in the boxes as it can be so simple and easy to forget once you've finished a box. 
* [Heath Adam's Ethical Hacking Course (aka TheCyberMentor)](https://www.udemy.com/course/practical-ethical-hacking/). Assumes you're a beginner to ethical hacking and teaches you everything you need to know about penetration testing for web and other applications. Especially useful if you're interested in pursuing the OSCP in the future. 
* [The Nightmare course](https://guyinatuxedo.github.io/) by my good friend guyinatuxedo. It is a comprehensive online book on getting into binary exploitation through exploring CTF challenges and various other real life examples. And one of the more beginner friendly guides for those interested in malware analysis and reverse engineering in the future. 
<br/>
## Level 3
* [HackTheBox](https://www.hackthebox.eu/). If you get stuck, there's always [Ippsec's videos](https://www.youtube.com/c/ippsec/playlists). Playing through the retired boxes is an especially good place to start off in HTB. 
* [Pwnable.kr](https://pwnable.kr/) for a cute and fun approach to pwning challenges and binary exploitation. 
* 

## Level 4 (Or more for deeper understanding of computer and systems internals as well as other specific fields)
* [Nand2Tetris](https://www.nand2tetris.org/) teaches you how to build a computer and OS from the ground up. A deep dive into operating systems. 
* For a hands-on and lecture based approach to going through The Web Application Hacker's Handbook (if you're interested in web), look no further than [Sam Bowne's Securing Web Applications](https://samsclass.info/129S/129S_F16.shtml). I personally couldn't get through the book at first but having a video and exercises to follow along with through reading the book helped immensely in understanding the concepts better. 
* [Awesome Gameboy Dev](https://project-awesome.org/gbdev/awesome-gbdev) for learning emulation, reverse engineering, and assembly and C for building and reversing all things Gameboys. 
* [Cryptohack](https://cryptohack.org/), a relatively new and very astounding website which teaches you cryptography through programming exercises (highly recommend the use of Python for this). Starts off easy but gets exponentially harder as you progress.
* [Trail of Bit's Guide on Forensics](https://trailofbits.github.io/ctf/forensics/). There's not much friendly guides on learning computer forensics out there for those who are interested, but this guide is about the only one I found that provides a comprehensive overview of how to approach forensics challenges for if you encounter one in CTFs. 
* [Systems Programming and Tools taught by Sanjiv Bhatia](http://www.cs.umsl.edu/~sanjiv/classes/cs2750/), lectures and walkthroughs on programming in the Linux/Unix environment. 
<br/>
## Some other fun sites to practice on
* [Hellbound Hackers](https://www.hellboundhackers.org/). Old fashioned but I somehow prefer it much more compared to HackThisSite!.
* [Enigma Group](https://www.enigmagroup.org/). Yet another web security training site but also I love the Alan Turing reference. 
* [Try2Hack](http://www.try2hack.nl/)
* [picoCTF](https://picoctf.com/). High school based CTF but also fun for beginners as well. Also great in exploring what topics you may be specifically interested in.
* [Don't forget to check for upcoming CTFs at ctftime.org!](http://ctftime.org/)
<br/>
Realistically, you could approach any of these resources in any order you prefer depending on your level of experience. This, though, provides to me at least a more structured and streamlined way of learning security concepts in a progressing manner. I hope this also helps future readers interested in also breaking into the field. This list may be edited in the future as needed.
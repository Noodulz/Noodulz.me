---
title: I've Gotten into Web CTFs Lately. Here are Some Common Techniques I've Learned
  So Far to Beat Them (For Clueless People!)
date: 2020-02-17 14:14:00 -05:00
---

![Nulab-Capture-the-Flag-CTF-Challenge-Blog.png](/uploads/Nulab-Capture-the-Flag-CTF-Challenge-Blog.png)

## What are CTFs???

For those of you who don't know, a CTF, or Capture The Flag (no, not the sport) is an online hacking game where the goal is to find your way through various systems to find a 'flag', or password to solving a level in the game. It is often played by security professionals and enthusiasts alike to practice their skills and most importantly, learn new ones along the way as they play. The games come in a couple categories: forensics, cryptography, misc., binary exploitation (AKA pwn, which so many guys here are suckers for!), and web.

So, the security team that I am active in here on campus was in need of someone who can complete web CTF challenges in particular, since there was an immense lack of that (because EVERYONE wants to do pwn and binary exploits mainly. For real). And given I've spent way too much time on the Internet as a kid and was on and off with web challs and CTFs over the years, I figured, why not take it seriously this time? Plus, DEFCON's Qualifiers are coming up right now, and I'd really like to contribute and compete somehow.

## A Few Good CTF Websites to Start Off In

I first found [Defend The Web!](https://defendtheweb.net) which is a terrific terrific (and I cannot stress enough, TERRIFIC) site that offers great web challenges for beginners as well as a forum to discuss and offer hints (during a challenge) and solutions (after you solve a challenge). They are fun if not brain-stumping, and get you to do a lot of Googling (which is okay by the way! You aren't expected to know EVERYTHING at first) to solve the challs. So far I'm almost 50% through, and can't wait to go through more.
![pico2.png](/uploads/pico2.png)
Then through a lot of my friends' recommendation, I started [PicoCTF](https://picoctf.com) which is a CTF game aimed at high schoolers and beginners. It offers a retro 8-bit like Unity game with a storyline to interact with the challenges as you solve them, which adds an extra layer of fun to approaching them in my opinion. I sought out the web exploitation challenges in particular, which start off really easy, much like Defend The Web, and then get progressively harder with having to Google a lot. However, the best hints are in the title of the challs themselves often, when it comes to Pico.

## Techniques

So! I'll get to the nitty gritty and explain the common techniques I've had to use in both those games:

* Check the source code by right clicking and then hitting 'Page Source' or 'Inspect Element'. Always do this first. Always. And read the source code closely. They will tell you everything you need to know to beat a level (well, more like offer weird formatted code for you to look into to exploit). And the beginner levels often have you searching the comments for the password, formatted as `<!--flag-->`. CTRL-F in source code is also another good thing to keep in mind.

* There will be a point where you will have to learn about Robot files that block certain access to directories in a website. Should be formatted as www.this-website.com/robots.txt.

* To create a basic POST form in HTML (think of your usual username and login page to send to a website as a request to login as user), open up a notepad or IDE and put this in:

  `<html>
  <!--This makes a password box and a submit button to send to a website-->
     <form action="link to website here" method="post">
     <label for="name">Password:</label><br/>
     <input type="text" name="password" /><br><br>
     <input type="submit" value="Submit">
     </form>
  </html>`

* For converting hashes and Base64s and Caesar Ciphers or anything like this, use this [godsend of a code cracking tool online](https://cryptii.com). Saves a lot of time. Caesar Ciphers are the ones often taught first so I recommend you get familiar with that early.

* Some challs will ask you to access a website as a certain user. For that, you will need to go into 'Inspect Element', find the Network Conditions, and edit the User Agent field to mask yourself as admin or another user they ask for.
  ![useragentdemo-e6bc0e.png](/uploads/useragentdemo-e6bc0e.png)

* All images have text in them. You can right click on an image on your desktop, click "Open With..." or something along those lines, and have the image opened in an IDE or Notepad. Some challs will have you investigate the insides of an image for the flag, and that will be one of the things you'll have to do.

* People's passwords on websites are often something about themselves or what they like. This makes for extremely weak passwords which you can bruteforce with. Keep that in mind.

* 24-bit files/images are a thing that can be reversed or converted back into a readable image.

* You will also learn a lot about SQL Injections, which are super important. They are commands that you enter into a search or login box in a website that bypasses the check and gets you vulnerable user data (and a flag!). A common SQL command I've found that seems to be used a lot is `SELECT * FROM Users WHERE UserId = 105 OR 1=1;`. [More on this here](https://www.w3schools.com/sql/sql_injection.asp).

* Google. Google and inspecting the page source are your two best friends in this game.

That's all I've found so far. So many times I've seen beginners at the security meetings I attend here get discouraged because they know absolutely nothing about where to look or what to know beforehand in solving a web challenge. And then they stop coming or leave defeated. So many of the professionals say you don't have to know anything, just a curiosity to learn. And they're right. But on the other hand, you're much less likely to give up and become more engaged if you've spent countless hours involved with programming and computer-related projects as a kid beforehand. Sure beginners are all welcome to learn and solve challenges, but how do you make them stick with it when they don't know anything at all or learned the perseverance in Googling and learning? I hope this article helps those beginners get over the obstacle and learning curve of diving into Web CTFs and challenges. And with that, I'll get back to rooting in web.
---
title: The Making of an Aggressively Encouraging(?) Mom (with Discord.js)
date: 2020-01-19 10:46:00 -05:00
---

For a while now, a certain group of friends of mine have asked for, quite literally, a bot that will tell motivate and encourage them to study. Normally this could've been done in a perfect world, where parents wholesomely support your goals and dreams and push you to be yourself and work hard. Right?

Wrong!! Not all parents are perfect. And so what better way to channel the inner traumas of the children of the world under strict parental guidance, than to build a stereotypical Asian mom bot in Discord that offensively berates you and passive aggressively encourages you to study?? 

Now all in all, this took about 8 hours of work, including figuring out how to parse key terms in messages using the Discord API and calling a random value from an array, as well as deploying it to AWS and other bot publishing sites. And I barely had or even remembered the Javascript syntax that I've been learning lately, so what better way than to practice my barely lingering JS skills by building such a heathen of a bot?<br/>
![kisspng-discord-computer-icons-logo-computer-software-avatar-5acbe3fc215959.1485806315233116121366.jpg](/uploads/kisspng-discord-computer-icons-logo-computer-software-avatar-5acbe3fc215959.1485806315233116121366.jpg)<br/>
So first, I had to skim some [Javascript references](https://htmlcheatsheet.com/js/). Just a brief catch up on what I'll be working with and to try and not get my fingers flied up in Java (as in mistakenly writing in Java and not JS). Then I was looking at more [guides](https://www.devdungeon.com/content/javascript-discord-bot-tutorial) and [outlines](https://www.sitepoint.com/discord-bot-node-js/) since I had no idea how to approach the [API](https://discordapp.com/developers/docs/intro) at first. Even after having gone through the basics of how to work with the bot to make it do what you want, I still wasn't getting to what I wanted to accomplish. And for a while it was just making this measly ping pong match with the bot:
```
var Discord = 
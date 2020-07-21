---
title: Pirates of The Memorial
date: 2020-07-17 17:33:00 -04:00
permalink: "/writeups/ctfs/csictf/osintone"
layout: post
---

So, my first instinct in approaching this challenge was of running through TinEye to see if the image popped up anywhere. Needless to say, nothing pulled up in the results. 
![tineye.png](/uploads/tineye.png)

My second instinct was to analyze the metadata and see if the photo had any hidden clues or information on the author. Yet, nothing pulled up as well, aside from the data info of the photo
![jfifmetadata.png](/uploads/jfifmetadata.png)

I looked through some other reverse image search engines and landed on Duplichecker. When loading the image, multiple results landed from different search engines, as compared to TinEye.
![duplichecker.png](/uploads/duplichecker.png)

I randomly picked Yandex, and the image popped up as the first result. When clicking on the image, it linked to a Twitter account which hosted the image. At first, it was much scrolling to find the original post. Then, I looked back at the Yandex result and found a link to the photo, which I overlooked originally. I landed on the Twitter post with the photo, and found the thread which then linked the author's Instagram account.
![twitterthread.png](/uploads/twitterthread.png)

Bingo. And when I go to look the author up on Instagram, lo and behold, in the comments section is the flag (which, was oddly placed a week ago from when the challenge started). 
![instagramflag.png](/uploads/instagramflag.png)

As someone who's been dabbling and trying at CTFs for so long, this was my actual first blood (no, I don't count the surveys and robot.txt challenges), so I am immensely relieved and proud and hope to go on and find more flags. 
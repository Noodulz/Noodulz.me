---
title: Project Euler 3
date: 2020-04-29 15:23:00 -04:00
permalink: "/writeups/ProjectEuler/ProjectEuler3"
layout: post
---

# Problem: The prime factors of 13195 are 5, 7, 13 and 29.

# What is the largest prime factor of the number 600851475143 ?

</br>

This one took a few hours of researching and figuring out. At first, I had tried a bruteforcing and direct method of trying to build a working method for the test case of 13195, which went something like this: 
<br/>
```
def prime(n):
   table = []
   for i in range(2, n):
      if(n % i == 0):
         for j in range(0, i):
            if(j / i != 0):
               table.append(i)
            elif (j / i == 0):
               break
    return table

prime(13195)
```

To which I got a table with the prime factors as exemplified in the problem, but also a lot of excess and leading 0's. And it took much too long overall to calculate. It was a helluva mess for sure. 
<br/>
And then with some research I figured that a while-loop thrown in would definitely cut down the time and increase efficiency in calculating the factors, as for-loops would be on a one by one basis in calculating whereas while-loops just go on until a certain point. 
<br/>
Solution:
<br/>
```
import math
def primeFactors(n): 
    for i in range(3,int(math.sqrt(n))+1,2): 
        while n % i== 0: 
            print(i) 
            n = n / i 
    if n > 2: 
        print(n)
primeFactors(600851475143) 
```

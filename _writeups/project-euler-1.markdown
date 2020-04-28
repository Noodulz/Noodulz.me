---
title: Project Euler 1
date: 2020-04-28 18:33:00 -04:00
permalink: "/writeups/ProjectEuler/ProjectEuler1"
layout: post
---

*Problem: If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.*

Implemented in Python 3. The problem is straight forward and asks to sum up any numbers that are a multiple of 3, and also a multiple of 5, which means we'd have to loop through numbers up to 1000 and add any numbers that are have a modulo of 0 when it comes to 3 or 5, even if the number is both a multiple of 3 and 5. 

Solution:
`i = 0
sum = 0

for i in range(0, 1000):
    if(i % 3 == 0 or i % 5 == 0):
        sum += i
print(sum)`
---
title: Project Euler 2
date: 2020-04-28 19:26:00 -04:00
permalink: "/writeups/ProjectEuler/ProjectEuler2"
layout: post
---

# Problem : Each new term in the Fibonacci sequence is generated by adding the previous two terms. By starting with 1 and 2, the first 10 terms will be:

# 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ...

# By considering the terms in the Fibonacci sequence whose values do not exceed four million, find the sum of the even-valued terms.
<br/>

This is not asking for the whole of the sum of the Fibonaaci numbers up till the term reaches 4000000 or above. But rather summing the specifically even terms within the sequence up until the even numbers reach 4000000 or above, to which it halts. So we'd have to use modulo once more to filter out the even numbers and sum them up in the sequence.
<br/>
Solution:
```
def fibby(n):
    first, second = 0 , 1
    fibnum = 0
    sum = 0
    if(n == 0):
        return one
    elif(n == 1):
        return two
    else:
        while(fibnum < n):
            fibnum = first + second
            first = second
            second = fibnum
            
            if(fibnum % 2 == 0):
                sum += fibnum           
    return sum

print(fibby(4000000))
```



---
title: Project Euler 4
date: 2020-04-29 20:17:00 -04:00
permalink: "/writeups/ProjectEuler/ProjectEuler4"
layout: post
---

# Problem: A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99.

# Find the largest palindrome made from the product of two 3-digit numbers.

<br/>

This one came a bit simpler to me compared to the last 3 problems. It was, to me, a matter of for-looping within for-looping the 3-digit numbers up to 999, and reversing them to check for a palindrome. At first, I had gotten the solution through the function returning a large list. However, I figured it would be much more clean and efficient to just return the max value from the list, and finish it at that.

<br/>
Solution:
<br/>
```
def hundredPalindrome():
  palindrome = []
  test = 0
  for i in range(100, 999):
    for j in range(100, 999):
      test = i * j 
      if(str(test) == str(test)[::-1]):
        palindrome.append(test)
  return max(palindrome)

print(hundredPalindrome())
    
```
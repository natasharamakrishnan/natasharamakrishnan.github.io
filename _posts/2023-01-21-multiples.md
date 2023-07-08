---
layout: post
title: Project Euler Question 1
tag: ["Project Euler"]
---

In this question, we are expected to obtain the sum of the multiples of 3 or
 5 below 1000.

``` python
def multiples():
    # answer will store the numbers as they're being added to each other.
    answer=0
    # number is being used to store the position in the range of the for loop.
    for number in range(1000):
        # checking which integers in the range are multiples of 3 or 5 and adding
        # them to the previously stored values.
        if number%3==0 or number%5==0:
            answer+=number
    
    return answer

result = multiples()
print(result)
```

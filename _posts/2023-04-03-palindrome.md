---
layout: post
title: Project Euler Question 4
tag: ["Project Euler"]
---

A number is said to be palindromic if it reads the same from left to right and right to left. For example, 1331 is a palindrome. In this question, we are required to find the largest palindrome constructed from the product of two 3-digit numbers.

```python
def product_of_integers():
    products=set()
    for i in range(100,1000):
        for j in range(100,1000):
            # ensuring the same two numbers aren't being multipled twice.
            if i>j:
                # products are converted to strings so they can 
                # be read forwards and backwards.
                num_string = str(i*j)
                if num_string == num_string[::-1]:
                    products.add(int(num_string))
    return products

numbers = product_of_integers()
print(max(numbers))
```
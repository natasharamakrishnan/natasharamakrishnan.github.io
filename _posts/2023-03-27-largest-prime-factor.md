---
layout: post
title: Project Euler Question 3
tag: ["Project Euler"]
---

In this question, we are being asked to acquire the largest prime factor of the integer 600851475143. A prime factor is a natural number whose only factors are 1 and itself. The first few prime factors are 2, 3, 5, and 7. The integer 1 is considered neither prime nor composite.

```python
def largest_prime_factor(n):
    # creating list of the range of integers from 2 to n
    prime_candidates=list(range(2,n))
    for candidate in prime_candidates:    
        for num in prime_candidates:
            if num != candidate and num%candidate==0:
                prime_candidates.remove(num)
    return prime_candidates

def get_factors(m):
    prime_factors=list(largest_prime_factor(m))
    prime_factors_set=set(prime_factors)
    for prime in prime_factors:
        if 600851475143%prime != 0:
            prime_factors_set.remove(prime)
    return prime_factors_set

m=int(600851475143**0.5+1)
output=(max(get_factors(m)))
print(output)

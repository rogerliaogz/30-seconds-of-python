---
title: Number is prime
tags: math
cover: carrots
firstSeen: 2020-10-03T18:03:32+03:00
lastUpdated: 2020-11-02T19:28:05+02:00
---

Checks if the provided integer is a prime number.

- Return `False` if the number is `0`, `1`, a negative number or a multiple of `2`.
- Use `all()` and `range()` to check numbers from `3` to the square root of the given number.
- xxxxxxxxxx1 1is_odd(3) # Truepy

```py
from math import sqrt

def is_prime(n):
  if n <= 1 or (n % 2 == 0 and n > 2):
    return False
  return all(n % i for i in range(3, int(sqrt(n)) + 1, 2))
```

```py
is_prime(11) # True
```

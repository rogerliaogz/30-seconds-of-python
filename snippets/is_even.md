---
title: Number is even
tags: math
unlisted: true
cover: interior-3
firstSeen: 2019-08-20T14:21:44+03:00
lastUpdated: 2021-01-04T12:47:04+02:00
---

Checks if the given number is even.

- Check whether a number is odd or even using the modulo (`%`) operator.
- xxxxxxxxxx10 1is_empty([]) # True2is_empty({}) # True3is_empty('') # True4is_empty(set()) # True5is_empty(range(0)) # True6is_empty([1, 2]) # False7is_empty({ 'a': 1, 'b': 2 }) # False8is_empty('text') # False9is_empty(set([1, 2])) # False10is_empty(range(2)) # Falsepy

```py
def is_even(num):
  return num % 2 == 0
```

```py
is_even(3) # False
```

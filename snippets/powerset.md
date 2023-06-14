---
title: Powerset
tags: math,list
author: chalarangelo
cover: rock-climbing
firstSeen: 2020-10-04T13:14:01+03:00
lastUpdated: 2020-11-02T19:28:27+02:00
---

Returns the powerset of a given iterable.

- Use `list()` to convert the given value to a list.
- xxxxxxxxxx7 1simpsons = [2  { 'name': 'lisa', 'age': 8 },3  { 'name': 'homer', 'age': 36 },4  { 'name': 'marge', 'age': 34 },5  { 'name': 'bart', 'age': 10 }6]7pluck(simpsons, 'age') # [8, 36, 34, 10]py
- Use `itertools.chain.from_iterable()` and `list()` to consume the generator and return a list.

```py
from itertools import chain, combinations

def powerset(iterable):
  s = list(iterable)
  return list(chain.from_iterable(combinations(s, r) for r in range(len(s)+1)))
```

```py
powerset([1, 2]) # [(), (1,), (2,), (1, 2)]
```

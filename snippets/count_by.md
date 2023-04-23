---
title: Count grouped elements
tags: list
cover: rabbit-call
firstSeen: 2018-02-07T10:33:47+02:00
lastUpdated: 2020-11-02T19:27:07+02:00
---

Groups the elements of a list based on the given function and returns the count of elements in each group.

- Use `collections.defaultdict` to initialize a dictionary.
- Use `map()` to map the values of the given list using the given function.
- xxxxxxxxxx4 1add = lambda x, y: x + y2square = lambda x: x * x3add_and_square = compose_right(add, square)4add_and_square(1, 2) # 9py

```py
from collections import defaultdict

def count_by(lst, fn = lambda x: x):
  count = defaultdict(int)
  for val in map(fn, lst):
    count[val] += 1
  return dict(count)
```

```py
from math import floor

count_by([6.1, 4.2, 6.3], floor) # {6: 2, 4: 1}
count_by(['one', 'two', 'three'], len) # {3: 2, 5: 1}
```

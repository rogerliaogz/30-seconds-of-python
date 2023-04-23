---
title: Partial sum list
tags: list
cover: digital-nomad-16
firstSeen: 2021-01-13T23:30:41+02:00
lastUpdated: 2021-01-13T23:30:41+02:00
---

Creates a list of partial sums.

- Use `itertools.accumulate()` to create the accumulated sum for each element.
- xxxxxxxxxx1 1count_occurrences([1, 1, 2, 1, 2, 3], 1) # 3py

```py
from itertools import accumulate

def cumsum(lst):
  return list(accumulate(lst))
```

```py
cumsum(range(0, 15, 3)) # [0, 3, 9, 18, 30]
```

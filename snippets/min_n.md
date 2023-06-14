---
title: N min elements
tags: list,math
cover: balloons
firstSeen: 2018-01-19T11:25:28+02:00
lastUpdated: 2020-11-02T19:28:27+02:00
---

Returns the `n` minimum elements from the provided list.

- Use `sorted()` to sort the list.
- Use slice notation to get the specified number of elements.
- Omit the second argument, `n`, to get a one-element list.
- xxxxxxxxxx1 1map_dictionary([1, 2, 3], lambda x: x * x) # { 1: 1, 2: 4, 3: 9 }py

```py
def min_n(lst, n = 1):
  return sorted(lst, reverse = False)[:n]
```

```py
min_n([1, 2, 3]) # [1]
min_n([1, 2, 3], 2) # [1, 2]
```

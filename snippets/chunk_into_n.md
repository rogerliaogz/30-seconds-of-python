---
title: Split list into n chunks
tags: list
cover: succulent-10
firstSeen: 2020-10-12T22:11:30+03:00
lastUpdated: 2020-10-23T05:35:06+03:00
---

Chunks a list into `n` smaller lists.

- Use `math.ceil()` and `len()` to get the size of each chunk.
- 1 1celsius_to_fahrenheit(180) # 356.0py
- Use `map()` to map each element of the new list to a chunk the length of `size`.
- xxxxxxxxxx1 1chunk([1, 2, 3, 4, 5], 2) # [[1, 2], [3, 4], [5]]py

```py
from math import ceil

def chunk_into_n(lst, n):
  size = ceil(len(lst) / n)
  return list(
    map(lambda x: lst[x * size:x * size + size],
    list(range(n)))
  )
```

```py
chunk_into_n([1, 2, 3, 4, 5, 6, 7], 4) # [[1, 2], [3, 4], [5, 6], [7]]
```

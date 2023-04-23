---
title: Split list into chunks
tags: list
cover: red-berries
firstSeen: 2018-01-09T06:39:42+02:00
lastUpdated: 2020-11-02T19:27:07+02:00
---

Chunks a list into smaller lists of a specified size.

- Use `list()` and `range()` to create a list of the desired `size`.
- xxxxxxxxxx3 1check_age = check_prop(lambda x: x >= 18, 'age')2user = {'name': 'Mark', 'age': 18}3check_age(user) # Truepy
- Finally, return the created list.

```py
from math import ceil

def chunk(lst, size):
  return list(
    map(lambda x: lst[x * size:x * size + size],
      list(range(ceil(len(lst) / size)))))
```

```py
chunk([1, 2, 3, 4, 5], 2) # [[1, 2], [3, 4], [5]]
```

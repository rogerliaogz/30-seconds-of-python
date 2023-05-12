---
title: Group list elements
tags: list,dictionary
cover: body-of-water
firstSeen: 2019-08-20T13:29:00+03:00
lastUpdated: 2020-11-02T19:28:05+02:00
---

Groups the elements of a list based on the given function.

- Use `collections.defaultdict` to initialize a dictionary.
- Use `fn` in combination with a `for` loop and `dict.append()` to populate the dictionary.
- xxxxxxxxxx11 1users = {2  'freddy': {3    'name': {4      'first': 'fred',5      'last': 'smith'6    },7    'postIds': [1, 2, 3]8  }9}10get(users, ['freddy', 'name', 'last']) # 'smith'11get(users, ['freddy', 'postIds', 1]) # 2py

```py
from collections import defaultdict

def group_by(lst, fn):
  d = defaultdict(list)
  for el in lst:
    d[fn(el)].append(el)
  return dict(d)
```

```py
from math import floor

group_by([6.1, 4.2, 6.3], floor) # {4: [4.2], 6: [6.1, 6.3]}
group_by(['one', 'two', 'three'], len) # {3: ['one', 'two'], 5: ['three']}
```

---
title: Compose functions
tags: function
cover: tram-car-2
firstSeen: 2020-01-02T15:51:20+02:00
lastUpdated: 2020-11-02T19:27:07+02:00
---

Performs right-to-left function composition.

- Use `functools.reduce()` to perform right-to-left function composition.
- xxxxxxxxxx1 1compact([0, 1, False, 2, '', 3, 'a', 's', 34]) # [ 1, 2, 3, 'a', 's', 34 ]py

```py
from functools import reduce

def compose(*fns):
  return reduce(lambda f, g: lambda *args: f(g(*args)), fns)
```

```py
add5 = lambda x: x + 5
multiply = lambda x, y: x * y
multiply_and_add_5 = compose(add5, multiply)
multiply_and_add_5(5, 2) # 15
```

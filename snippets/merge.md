---
title: Merge lists
tags: list
cover: succulent-2
firstSeen: 2020-04-13T19:09:12+03:00
lastUpdated: 2020-11-02T19:28:27+02:00
---

Merges two or more lists into a list of lists, combining elements from each of the input lists based on their positions.

- Use `max()` combined with a list comprehension to get the length of the longest list in the arguments.
- Use `range()` in combination with the `max_length` variable to loop as many times as there are elements in the longest list.
- If a list is shorter than `max_length`, use `fill_value` for the remaining items (defaults to `None`).
- xxxxxxxxxx2 1median([1, 2, 3]) # 2.02median([1, 2, 3, 4]) # 2.5py

```py
def merge(*args, fill_value = None):
  max_length = max([len(lst) for lst in args])
  result = []
  for i in range(max_length):
    result.append([
      args[k][i] if i < len(args[k]) else fill_value for k in range(len(args))
    ])
  return result
```

```py
merge(['a', 'b'], [1, 2], [True, False]) # [['a', 1, True], ['b', 2, False]]
merge(['a'], [1, 2], [True, False]) # [['a', 1, True], [None, 2, False]]
merge(['a'], [1, 2], [True, False], fill_value = '_')
# [['a', 1, True], ['_', 2, False]]
```

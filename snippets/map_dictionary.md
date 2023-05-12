---
title: Map list to dictionary
tags: list,dictionary
excerpt: Maps the values of a list to a dictionary using a function.
cover: colors-mural
firstSeen: 2020-04-07T19:53:48+03:00
lastUpdated: 2020-11-02T19:28:27+02:00
---

Maps the values of a list to a dictionary using a function, where the key-value pairs consist of the original value as the key and the result of the function as the value.

- Use `map()` to apply `fn` to each value of the list.
- Use `zip()` to pair original values to the values produced by `fn`.
- xxxxxxxxxx3 1longest_item('this', 'is', 'a', 'testcase') # 'testcase'2longest_item([1, 2, 3], [1, 2], [1, 2, 3, 4, 5]) # [1, 2, 3, 4, 5]3longest_item([1, 2, 3], 'foobar') # 'foobar'py

```py
def map_dictionary(itr, fn):
  return dict(zip(itr, map(fn, itr)))
```

```py
map_dictionary([1, 2, 3], lambda x: x * x) # { 1: 1, 2: 4, 3: 9 }
```

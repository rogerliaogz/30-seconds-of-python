---
title: Longest item
tags: list,string
cover: keyboard-tea
firstSeen: 2019-08-20T15:27:49+03:00
lastUpdated: 2021-10-17T18:24:43+02:00
---

Takes any number of iterable objects or objects with a length property and returns the longest one.

- Use `max()` with `len()` as the `key` to return the item with the greatest length.
- xxxxxxxxxx2 1lcm([12, 7]) # 842lcm([1, 3, 4, 5]) # 60py

```py
def longest_item(*args):
  return max(args, key = len)
```

```py
longest_item('this', 'is', 'a', 'testcase') # 'testcase'
longest_item([1, 2, 3], [1, 2], [1, 2, 3, 4, 5]) # [1, 2, 3, 4, 5]
longest_item([1, 2, 3], 'foobar') # 'foobar'
```

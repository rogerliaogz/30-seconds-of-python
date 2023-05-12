---
title: Dictionary keys
tags: dictionary,list
cover: succulent-5
firstSeen: 2018-04-01T23:56:31+03:00
lastUpdated: 2020-11-02T19:28:05+02:00
---

Creates a flat list of all the keys in a flat dictionary.

- Use `dict.keys()` to return the keys in the given dictionary.
- xxxxxxxxxx1 1key_of_min({'a':4, 'b':0, 'c':13}) # bpy

```py
def keys_only(flat_dict):
  return list(flat_dict.keys())
```

```py
ages = {
  'Peter': 10,
  'Isabel': 11,
  'Anna': 9,
}
keys_only(ages) # ['Peter', 'Isabel', 'Anna']
```

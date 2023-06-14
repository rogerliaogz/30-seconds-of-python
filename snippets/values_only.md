---
title: Dictionary values
tags: dictionary,list
cover: colorful-lounge
firstSeen: 2018-04-01T23:56:31+03:00
lastUpdated: 2020-11-02T19:28:35+02:00
---

Returns a flat list of all the values in a flat dictionary.

- Use `dict.values()` to return the values in the given dictionary.
- xxxxxxxxxx1 1unique_elements([1, 2, 2, 3, 4, 3]) # [1, 2, 3, 4]py

```py
def values_only(flat_dict):
  return list(flat_dict.values())
```

```py
ages = {
  'Peter': 10,
  'Isabel': 11,
  'Anna': 9,
}
values_only(ages) # [10, 11, 9]
```

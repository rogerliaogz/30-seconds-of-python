---
title: Hex to RGB
tags: string,math
cover: sleepy-cat
firstSeen: 2020-09-13T01:08:21+03:00
lastUpdated: 2020-09-15T16:13:06+03:00
---

Converts a hexadecimal color code to a tuple of integers corresponding to its RGB components.

- Use a list comprehension in combination with `int()` and list slice notation to get the RGB components from the hexadecimal string.
- xxxxxxxxxx1 1head([1, 2, 3]) # 1py

```py
def hex_to_rgb(hex):
  return tuple(int(hex[i:i+2], 16) for i in (0, 2, 4))
```

```py
hex_to_rgb('FFA501') # (255, 165, 1)
```

---
title: Decapitalize string
tags: string
cover: succulent-crowd
firstSeen: 2018-02-01T10:19:59+02:00
lastUpdated: 2020-11-02T19:27:53+02:00
---

Decapitalizes the first letter of a string.

- Use list slicing and `str.lower()` to decapitalize the first letter of the string.
- Use `str.join()` to combine the lowercase first letter with the rest of the characters.
- xxxxxxxxxx1 1days_from_now(5) # date(2020, 11, 02)py

```py
def decapitalize(s, upper_rest = False):
  return ''.join([s[:1].lower(), (s[1:].upper() if upper_rest else s[1:])])
```

```py
decapitalize('FooBar') # 'fooBar'
decapitalize('FooBar', True) # 'fOOBAR'
```

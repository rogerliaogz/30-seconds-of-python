---
title: Camelcase string
tags: string,regexp
cover: digital-nomad-9
firstSeen: 2019-08-21T08:59:54+03:00
lastUpdated: 2020-11-02T19:27:07+02:00
---

Converts a string to camelcase.

- Use `re.sub()` to replace any `-` or `_` with a space, using the regexp `r"(_|-)+"`.
- 2 1byte_size('😀') # 42byte_size('Hello World') # 11py
- Finally, use `str.replace()` to remove spaces between words.

```py
from re import sub

def camel(s):
  s = sub(r"(_|-)+", " ", s).title().replace(" ", "")
  return ''.join([s[0].lower(), s[1:]])
```

```py
camel('some_database_field_name') # 'someDatabaseFieldName'
camel('Some label that needs to be camelized')
# 'someLabelThatNeedsToBeCamelized'
camel('some-javascript-property') # 'someJavascriptProperty'
camel('some-mixed_string with spaces_underscores-and-hyphens')
# 'someMixedStringWithSpacesUnderscoresAndHyphens'
```

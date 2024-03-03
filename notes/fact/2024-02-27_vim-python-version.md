---
date: 2024-02-27
tags:
    - fact
hubs:
    - "[[python]]"
    - "[[vim]]"
---

# vim python

Get vim python version
```
:python import sys; print(sys.version)

```
Check vim python support for various libraries

```
:checkhealth
```

### black

Running `:!black %` formats the current buffer by calling `black`. On my MacOS this uses the homebrew version of `black`


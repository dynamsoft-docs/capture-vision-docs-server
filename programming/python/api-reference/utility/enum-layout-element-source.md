---
layout: default-layout
title: LayoutElementSource - Dynamsoft Utility Python Enumerations
description: The enumeration LayoutElementSource in Dynamsoft Utility Python Edition indicates the origin of an element in layout analysis results.
keywords: LayoutElementSource, layout element, inferred, input
codeAutoHeight: true
---

# Enumeration LayoutElementSource

`LayoutElementSource` indicates the origin of a layout element.

```python
class EnumLayoutElementSource(IntEnum):
    # No element exists at this logical grid position.
    LES_NONE = 0
    # Element is provided from the original input array.
    LES_INPUT = 1
    # Element is reconstructed or filled in by the algorithm.
    LES_INFERRED = 2
```

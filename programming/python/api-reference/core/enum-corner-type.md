---
layout: default-layout
title: CornerType - Dynamsoft Core Python Enumerations
description: The enumeration CornerType in Dynamsoft Core Python Edition describes how a corner is geometrically formed by its two sides.
keywords: Corner type
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

```python
class EnumCornerType(IntEnum):
   # The sides of the corner is normally intersected.
   CT_NORMAL_INTERSECTED
   # The sides of the corner is T-intersected.
   CT_T_INTERSECTED
   # The sides of the corner is cross-intersected.
   CT_CROSS_INTERSECTED
   # The sides are not intersected but they definitely make up a corner.
   CT_NOT_INTERSECTED
```
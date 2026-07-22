---
layout: default-layout
title: MeasureUnit - Dynamsoft Core Python Enumerations
description: The enumeration MeasureUnit in Dynamsoft Core Python Edition specifies how a numeric value is interpreted relative to a reference dimension.
keywords: MeasureUnit, pixel, percentage
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension.

```python
class EnumMeasureUnit(IntEnum):
    # The value is an absolute pixel count.
    MU_PIXEL = 0
    # The value is a percentage of the reference dimension (e.g. 25 = 25%).
    MU_PERCENTAGE = 1
```

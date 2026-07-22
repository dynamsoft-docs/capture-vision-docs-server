---
layout: default-layout
title: LayoutPattern - Dynamsoft Utility Python Enumerations
description: The enumeration LayoutPattern in Dynamsoft Utility Python Edition defines strategies for organizing quadrilaterals in layout analysis.
keywords: LayoutPattern, layout, lines, matrix
codeAutoHeight: true
---

# Enumeration LayoutPattern

`LayoutPattern` defines the strategy for the layout engine to organize quadrilaterals.

```python
class EnumLayoutPattern(IntEnum):
    # Algorithm automatically detects the best layout pattern.
    LP_UNKNOWN = 0
    # Elements are organized into sequential lines (rows or columns).
    LP_LINES = 1
    # Elements are organized into a strict grid/matrix structure.
    LP_MATRIX = 2
```

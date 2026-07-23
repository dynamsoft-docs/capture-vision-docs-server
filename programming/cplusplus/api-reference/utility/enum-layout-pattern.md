---
layout: default-layout
title: LayoutPattern - Dynamsoft Utility Enumerations
description: Reference for the LayoutPattern enumeration in Dynamsoft Utility C++ Edition, defining strategies for organizing quadrilaterals in layout analysis.
keywords: LayoutPattern, layout, lines, matrix
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration LayoutPattern

`LayoutPattern` defines the strategy for the layout engine to organize quadrilaterals.

```cpp
typedef enum LayoutPattern
{
    /** Algorithm automatically detects the best layout pattern. */
    LP_UNKNOWN = 0,
    /** Elements are organized into sequential lines (rows or columns). */
    LP_LINES   = 1,
    /** Elements are organized into a strict grid/matrix structure. */
    LP_MATRIX  = 2
} LayoutPattern;
```

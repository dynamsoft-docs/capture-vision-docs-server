---
layout: default-layout
title: LayoutPattern - Dynamsoft Utility Java Enumerations
description: The enumeration LayoutPattern in Dynamsoft Utility Java Edition defines strategies for organizing quadrilaterals in layout analysis.
keywords: LayoutPattern, layout, lines, matrix
codeAutoHeight: true
---

# Enumeration LayoutPattern

`LayoutPattern` defines the strategy for the layout engine to organize quadrilaterals.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumLayoutPattern {
    /** Algorithm automatically detects the best layout pattern. */
    int LP_UNKNOWN = 0;
    /** Elements are organized into sequential lines (rows or columns). */
    int LP_LINES = 1;
    /** Elements are organized into a strict grid/matrix structure. */
    int LP_MATRIX = 2;
}
```

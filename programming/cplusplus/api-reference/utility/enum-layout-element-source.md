---
layout: default-layout
title: LayoutElementSource - Dynamsoft Utility Enumerations
description: Reference for the LayoutElementSource enumeration in Dynamsoft Utility C++ Edition, indicating the origin of an element in layout analysis results.
keywords: LayoutElementSource, layout element, inferred, input
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration LayoutElementSource

`LayoutElementSource` indicates the origin of a layout element.

```cpp
typedef enum LayoutElementSource
{
    /** No element exists at this logical grid position (used for alignment in non-uniform rows). */
    LES_NONE     = 0,
    /** Element is provided from the original input array. */
    LES_INPUT    = 1,
    /** Element is reconstructed or filled in by the algorithm. */
    LES_INFERRED = 2
} LayoutElementSource;
```

---
layout: default-layout
title: LayoutElementSource - Dynamsoft Utility Java Enumerations
description: The enumeration LayoutElementSource in Dynamsoft Utility Java Edition indicates the origin of an element in layout analysis results.
keywords: LayoutElementSource, layout element, inferred, input
codeAutoHeight: true
---

# Enumeration LayoutElementSource

`LayoutElementSource` indicates the origin of a layout element.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumLayoutElementSource {
    /** No element exists at this logical grid position (used for alignment in non-uniform rows). */
    int LES_NONE = 0;
    /** Element is provided from the original input array. */
    int LES_INPUT = 1;
    /** Element is reconstructed or filled in by the algorithm. */
    int LES_INFERRED = 2;
}
```

---
layout: default-layout
title: CornerType - Dynamsoft Core Java Enumerations
description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

```java
@Retention(RetentionPolicy.CLASS)
@Target(ElementType.FIELD)
public @interface EnumCornerType {
    //The sides of the corner is normally intersected.
    int CT_NORMAL_INTERSECTED = 0;
    //The sides of the corner is T-intersected.
    int CT_T_INTERSECTED = 1;
    //The sides of the corner is cross-intersected.
    int CT_CROSS_INTERSECTED = 2;
    //The sides are not intersected but they definitely make up a corner.
    int CT_NOT_INTERSECTED = 3;
}
```
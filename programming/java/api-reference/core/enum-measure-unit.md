---
layout: default-layout
title: MeasureUnit - Dynamsoft Core Java Enumerations
description: The enumeration MeasureUnit in Dynamsoft Core Java Edition specifies how a numeric value is interpreted relative to a reference dimension.
keywords: MeasureUnit, pixel, percentage
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumMeasureUnit {
    /** The value is an absolute pixel count. */
    int MU_PIXEL = 0;
    /** The value is a percentage of the reference dimension (e.g. 25 = 25%). */
    int MU_PERCENTAGE = 1;
}
```

---
layout: default-layout
title: MeasureUnit - Dynamsoft Core Enumerations
description: Reference for the MeasureUnit enumeration in Dynamsoft Core C++ Edition, specifying how a numeric value is interpreted relative to a reference dimension.
keywords: MeasureUnit, pixel, percentage
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: MeasureUnit
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension. It is used wherever a numeric parameter (e.g., spacing, ROI coordinates) can be expressed either as an absolute pixel count or as a proportion of a reference size.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum MeasureUnit
{
    /** The value is an absolute pixel count. */
    MU_PIXEL      = 0,
    /** The value is a percentage of the reference dimension (e.g. 25 = 25%). */
    MU_PERCENTAGE = 1
} MeasureUnit;
```

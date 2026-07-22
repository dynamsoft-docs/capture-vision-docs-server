---
layout: default-layout
title: MeasureUnit - Dynamsoft Core .NET Enumerations
description: The enumeration MeasureUnit in Dynamsoft Core .NET Edition specifies how a numeric value is interpreted relative to a reference dimension.
keywords: MeasureUnit, pixel, percentage
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension.

```csharp
public enum MeasureUnit
{
   /** The value is an absolute pixel count. */
   MU_PIXEL = 0,
   /** The value is a percentage of the reference dimension (e.g. 25 = 25%). */
   MU_PERCENTAGE = 1
}
```

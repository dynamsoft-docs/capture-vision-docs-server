---
layout: default-layout
title: CornerType - Dynamsoft Core .NET Enumerations
description: The enumeration CornerType describes how the corner is formed by its sides for .NET Edition.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

```csharp
public enum EnumCornerType
{
   /* The sides of the corner is normally intersected. */
   CT_NORMAL_INTERSECTED = 0,
   /* The sides of the corner is T-intersected. */
   CT_T_INTERSECTED = 1,
   /* The sides of the corner is cross-intersected. */
   CT_CROSS_INTERSECTED = 2,
   /* The sides are not intersected but they definitely make up a corner. */
   CT_NOT_INTERSECTED = 3
}
```
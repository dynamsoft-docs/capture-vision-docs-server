---
layout: default-layout
title: CornerType - Dynamsoft Core Enumerations
description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum CornerType
{
   /* The sides of the corner is normally intersected. */
   CT_NORMAL_INTERSECTED = 0,
   /* The sides of the corner is T-intersected. */
   CT_T_INTERSECTED = 1,
   /* The sides of the corner is cross-intersected. */
   CT_CROSS_INTERSECTED = 2,
   /* The sides are not intersected but they definitely make up a corner. */
   CT_NOT_INTERSECTED = 3,
} CornerType;
```
---
layout: default-layout
title: FilterType - Dynamsoft Utility Enumerations
description: The enumeration FilterType of Dynamsoft Utility describes the specified image filter applied to an input image.
keywords: image filter
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` describes the specified image filter applied to an input image.

```java
@interface EnumFilterType {
   // High-pass filter: Enhances edges and fine details by attenuating low-frequency components.
   int FT_HIGH_PASS = 0;
   // Sharpen filter: Increases contrast along edges to make the image appear more defined.
   int FT_SHARPEN = 1;
   // Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.
   int FT_SMOOTH = 2;
}
```

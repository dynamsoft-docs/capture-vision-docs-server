---
layout: default-layout
title: FilterType - Dynamsoft Utility Enumerations
description: The enumeration FilterType of Dynamsoft Utility describes the specified image filter applied to an input image.
keywords: image filter
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` describes the specified image filter applied to an input image.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum FilterType
{
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   FT_HIGH_PASS,
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   FT_SHARPEN,
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   FT_SMOOTH
}FilterType;
```

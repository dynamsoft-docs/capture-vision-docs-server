---
layout: default-layout
title: FilterType - Dynamsoft Utility .NET Enumerations
description: The enumeration FilterType in Dynamsoft Utility .NET Edition specifies the type of image filter applied during image processing operations.
keywords: image filter
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` describes the specified image filter applied to an input image.

```csharp
public enum EnumFilterType
{
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   FT_HIGH_PASS,
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   FT_SHARPEN,
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   FT_SMOOTH
}
```

---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core .NET Enumerations
description: The enumeration GrayscaleTransformationMode describes all available grayscale transformation modes for .NET Edition.
keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

```csharp
public enum EnumGrayscaleTransformationMode
{
   /** Transforms to inverted grayscale. Recommended for light on dark images. */
   GTM_INVERTED = 0x01,
   /** Keeps the original grayscale. Recommended for dark on light images. */
   GTM_ORIGINAL = 0x02,
   /** Lets the library choose an algorithm automatically for grayscale transformation. */
   GTM_AUTO = 0x04,
   /**Placeholder value with no functional meaning. */
   GTM_END = -1,
   /** Reserved setting for grayscale transformation mode. */
   GTM_REV = -2147483648,
   /** Skips grayscale transformation. */
   GTM_SKIP = 0x00
}
```
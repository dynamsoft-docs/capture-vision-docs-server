---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core .NET Enumerations
description: The enumeration GrayscaleEnhancementMode describes all available grayscale enhancement modes for .NET Edition.
keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

```csharp
public enum EnumGrayscaleEnhancementMode
{
   /**Not supported yet. */
   GEM_AUTO = 0x01,
   /**Takes the unpreprocessed image for following operations. */
   GEM_GENERAL = 0x02,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_EQUALIZE = 0x04,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_SMOOTH = 0x08,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_SHARPEN_SMOOTH = 0x10,
   /**Placeholder value with no functional meaning. */
   GEM_END = -1,
   /**Reserved setting for image preprocessing mode.*/
   GEM_REV = -2147483648,
   /**Skips image preprocessing. */
   GEM_SKIP = 0x00
}
```
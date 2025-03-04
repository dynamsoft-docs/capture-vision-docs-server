---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum GrayscaleEnhancementMode
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
#if defined(_WIN32) || defined(_WIN64)
   GEM_END = 0xFFFFFFFF,
#else
   GEM_END = -1,
#endif
   /**Reserved setting for image preprocessing mode.*/
#if defined(_WIN32) || defined(_WIN64)
   GEM_REV = 0x80000000,
#else
   GEM_REV = -2147483648,
#endif
   /**Skips image preprocessing. */
   GEM_SKIP = 0x00
}GrayscaleEnhancementMode;
```
---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Python Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

```python
class EnumGrayscaleEnhancementMode(IntEnum):
    #Not supported yet. 
    GEM_AUTO = 0x01
    #Takes the unpreprocessed image for following operations. 
    GEM_GENERAL = 0x02
    #Preprocesses the image using the gray equalization algorithm.
    GEM_GRAY_EQUALIZE = 0x04
    #Preprocesses the image using the gray smoothing algorithm.
    GEM_GRAY_SMOOTH = 0x08
    #Preprocesses the image using the sharpening and smoothing algorithm.
    GEM_SHARPEN_SMOOTH = 0x10
    #Reserved setting for image preprocessing mode.
    GEM_REV = -2147483648
    #Skips image preprocessing. 
    GEM_SKIP = 0x00
```
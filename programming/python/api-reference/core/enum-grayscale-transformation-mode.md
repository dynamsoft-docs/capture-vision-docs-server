---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core Python Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

```python
class EnumGrayscaleTransformationMode(IntEnum):
    #Transforms to inverted grayscale. Recommended for light on dark images. 
    GTM_INVERTED = 0x01
    #Keeps the original grayscale. Recommended for dark on light images. 
    GTM_ORIGINAL = 0x02
    #Lets the library choose an algorithm automatically for grayscale transformation.
    GTM_AUTO = 0x04
    #Reserved setting for grayscale transformation mode.
    GTM_REV = -2147483648
    #Skips grayscale transformation. 
    GTM_SKIP = 0x00
```
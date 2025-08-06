---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Java Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumGrayscaleEnhancementMode {
    //Skips image preprocessing. 
    int GEM_SKIP = 0x00;
    //Not supported yet. 
    int GEM_AUTO = 0x01;
    //Takes the unpreprocessed image for following operations. 
    int GEM_GENERAL = 0x02;
    //Preprocesses the image using the gray equalization algorithm.
    int GEM_GRAY_EQUALIZE = 0x04;
    //Preprocesses the image using the gray smoothing algorithm.
    int GEM_GRAY_SMOOTH = 0x08;
    //Preprocesses the image using the sharpening and smoothing algorithm.
    int GEM_SHARPEN_SMOOTH = 0x10;
    //Reserved setting for image preprocessing mode.
    int GEM_REV = 0x80000000;
    //End marker for enumeration.
    int GEM_END = 0xFFFFFFFF;
}
```
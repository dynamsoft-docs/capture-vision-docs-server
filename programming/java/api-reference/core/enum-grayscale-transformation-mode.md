---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core Java Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumGrayscaleTransformationMode {
    //Skips grayscale transformation. 
    int GTM_SKIP = 0x00;
    //Transforms to inverted grayscale. Recommended for light on dark images. 
    int GTM_INVERTED = 0x01;
    //Keeps the original grayscale. Recommended for dark on light images. 
    int GTM_ORIGINAL = 0x02;
    //Lets the library choose an algorithm automatically for grayscale transformation.
    int GTM_AUTO = 0x04;
    //Reserved setting for grayscale transformation mode.
    int GTM_REV = 0x80000000;
    //End marker for enumeration.
    int GTM_END = 0xFFFFFFFF;
}
```
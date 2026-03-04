---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core Java Enumerations
description: The enumeration ImageCaptureDistanceMode in Dynamsoft Core Java Edition distinguishes close-up captures from long-distance captures to optimize image processing.
keywords: Image capture distance
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageCaptureDistanceMode {
    //The image is taken by close-up shot camera.
    int ICDM_NEAR = 0;
    //The image is taken by long shot camera.
    int ICDM_FAR = 1;
}
```

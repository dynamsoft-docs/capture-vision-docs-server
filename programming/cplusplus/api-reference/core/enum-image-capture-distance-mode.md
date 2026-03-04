---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core Enumerations
description: Reference for the ImageCaptureDistanceMode enumeration in Dynamsoft Core C++ Edition, distinguishing close-up from long-distance image captures to optimize processing.
keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageCaptureDistanceMode
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum ImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   ICDM_NEAR,
   /** The image is taken by long shot camera. */
   ICDM_FAR
} CaptureDistanceMode;
```

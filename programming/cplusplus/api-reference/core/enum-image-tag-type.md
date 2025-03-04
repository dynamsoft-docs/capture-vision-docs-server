---
layout: default-layout
title: ImageTagType - Dynamsoft Core Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum ImageTagType
{
   /**Represents an image that has been sourced from a static file.*/
   ITT_FILE_IMAGE,
   /**Indicates that the image is a frame extracted from a video stream.*/
   ITT_VIDEO_FRAME
} ImageTagType;
```
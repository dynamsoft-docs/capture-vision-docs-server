---
layout: default-layout
title: ImageTagType - Dynamsoft Core .NET Enumerations
description: The enumeration ImageTagType describes the types of image tags for .NET Edition.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

```csharp
public enum EnumImageTagType
{
   /**Represents an image that has been sourced from a static file.*/
   ITT_FILE_IMAGE,
   /**Indicates that the image is a frame extracted from a video stream.*/
   ITT_VIDEO_FRAME
}
```
---
layout: default-layout
title: ImageTagType - Dynamsoft Core Java Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
keywords: Image tag type
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageTagType {
    //The image is a file image.
    int ITT_FILE_IMAGE = 0;
    //The image is a video frame.
    int ITT_VIDEO_FRAME = 1;
}
```
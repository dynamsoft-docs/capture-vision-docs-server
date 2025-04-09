---
layout: default-layout
title: ImageTagType - Dynamsoft Core Python Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
keywords: Image tag type
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

```python
class EnumImageTagType(IntEnum):
    #The image is a file image.
    ITT_FILE_IMAGE
    #The image is a video frame.
    ITT_VIDEO_FRAME
```
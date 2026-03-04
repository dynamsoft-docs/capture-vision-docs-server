---
layout: default-layout
title: VideoFrameQuality - Dynamsoft Core Enumerations
description: The enumeration VideoFrameQuality in Dynamsoft Core Python Edition classifies video frame quality (high or low) to control which frames are processed.
keywords: Video frame quality
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: VideoFrameQuality
codeAutoHeight: true
---

# Enumeration VideoFrameQuality

`VideoFrameQuality` describes the quality of video frames.

```python
class EnumVideoFrameQuality(IntEnum):
    #The frame quality is measured to be high.
    VFQ_HIGH
    #The frame quality is measured to be low.
    VFQ_LOW
    #The frame quality is unknown.
    VFQ_UNKNOWN
```
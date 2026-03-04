---
layout: default-layout
title: VideoFrameQuality - Dynamsoft Core Enumerations
description: Reference for the VideoFrameQuality enumeration in Dynamsoft Core C++ Edition, classifying video frame quality (high or low) to control which frames are processed.
keywords: Video frame quality
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: VideoFrameQuality
codeAutoHeight: true
---

# Enumeration VideoFrameQuality

`VideoFrameQuality` describes the quality of video frames.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum VideoFrameQuality {
   /**The frame quality is measured to be high.*/
   VFQ_HIGH,
   /**The frame quality is measured to be low.*/
   VFQ_LOW,
   /**The frame quality is unknown.*/
   VFQ_UNKNOWN
} VideoFrameQuality;
```
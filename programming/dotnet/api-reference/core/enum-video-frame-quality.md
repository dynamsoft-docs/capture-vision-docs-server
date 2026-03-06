---
layout: default-layout
title: VideoFrameQuality - Dynamsoft Core .NET Enumerations
description: The enumeration VideoFrameQuality in Dynamsoft Core .NET Edition classifies video frame quality (high or low) to control which frames are processed.
keywords: Video frame quality
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration VideoFrameQuality

`VideoFrameQuality` describes the quality of video frames.

```csharp
public enum EnumVideoFrameQuality
{
   /**The frame quality is measured to be high.*/
   VFQ_HIGH,
   /**The frame quality is measured to be low.*/
   VFQ_LOW,
   /**The frame quality is unknown.*/
   VFQ_UNKNOWN
}
```
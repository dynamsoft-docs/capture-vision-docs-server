---
layout: default-layout
title: ImageSourceState - Dynamsoft Vision Router .NET Enumerations
description: The enumeration ImageSourceState in Dynamsoft Capture Vision .NET Edition describes the possible states of the ImageSourceAdapter (exhausted or buffered).
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ImageSourceState

`ImageSourceState` describes the state of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

```csharp
public enum EnumImageSourceState
{
   /** Indicates that the buffer of the image source is currently empty. */
   ISS_BUFFER_EMPTY,
   /** Signifies that the source for the image source has been depleted. */
   ISS_EXHAUSTED
}
```
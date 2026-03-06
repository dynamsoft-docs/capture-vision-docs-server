---
layout: default-layout
title: ImageSourceState - Dynamsoft Core C++ Enumerations
description: Reference for the ImageSourceState enumeration in Dynamsoft Capture Vision C++ Edition, describing the states of the ImageSourceAdapter (exhausted, buffered).
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
codeAutoHeight: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the state of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum ImageSourceState
{
   /** Indicates that the buffer of the image source is currently empty. */
   ISS_BUFFER_EMPTY,
   /** Signifies that the source for the image source has been depleted. */
   ISS_EXHAUSTED
} ImageSourceState;
```
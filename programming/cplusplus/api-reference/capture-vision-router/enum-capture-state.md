---
layout: default-layout
title: CaptureState - Dynamsoft Vision Router C++ Enumerations
description: Reference for the CaptureState enumeration in Dynamsoft Capture Vision C++ Edition, describing the possible states of the data capture process (started, stopped).
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CaptureState
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum CaptureState
{
   /** The data capturing is started. */
   CS_STARTED,
   /** The data capturing is stopped. */
   CS_STOPPED,
   /**The data capturing is paused.*/
   CS_PAUSED,
   /**The data capturing is resumed.*/
   CS_RESUMED
} CaptureState;
```
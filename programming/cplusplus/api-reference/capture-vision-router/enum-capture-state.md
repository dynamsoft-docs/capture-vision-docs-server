---
layout: default-layout
title: CaptureState - Dynamsoft Vision Router Enumerations
description: The enumeration CaptureState of Dynamsoft Vision Router describes the state of data capturing.
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
---
layout: default-layout
title: CaptureState - Dynamsoft Vision Router Java Enumerations
description: The enumeration CaptureState of Dynamsoft Vision Router describes the state of data capturing.
keywords: Capture state
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

```java
@interface EnumCaptureState {
    //The data capturing is started.
    int CS_STARTED = 0;
    //The data capturing is stopped.
    int CS_STOPPED = 1;
    //The data capturing is paused.
    int CS_PAUSED = 2;
    //The data capturing is resumed.
    int CS_RESUMED = 3;
}
```
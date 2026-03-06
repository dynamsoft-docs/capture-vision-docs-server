---
layout: default-layout
title: CaptureState - Dynamsoft Vision Router Python Enumerations
description: The enumeration CaptureState in Dynamsoft Capture Vision Python Edition describes the possible states of the data capture process (started, stopped, paused, resumed).
keywords: Capture state
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

```python
class EnumCaptureState(IntEnum):
    #The data capturing is started.
    CS_STARTED
    #The data capturing is stopped.
    CS_STOPPED
    #The data capturing is paused.
    CS_PAUSED
    #The data capturing is resumed.
    CS_RESUMED
```
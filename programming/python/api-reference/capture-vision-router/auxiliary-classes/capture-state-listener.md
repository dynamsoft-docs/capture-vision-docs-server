---
layout: default-layout
title: CaptureStateListener Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CaptureStateListener class in Dynamsoft Capture Vision Module Python Edition.
keywords: capture state listener, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureStateListener

Defines a listener for capture state changes. 

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class CaptureStateListener(ABC)
```

## Methods

| Method                                            | Description                            |
| ------------------------------------------------- | -------------------------------------- |
| [`on_capture_state_changed`](#on_capture_state_changed) | Called when the capture state changes. |

### on_capture_state_changed

Called when the capture state changes.

```python
@abstractmethod
def on_capture_state_changed(self, state: int) -> None:
```

**Parameters**

`state` The new capture state. It is one of the values of the `EnumCaptureState` enumeration.

**See Also**

[EnumCaptureState]({{ site.dcvb_enumerations }}capture-vision-router/capture-state.html?lang=python)
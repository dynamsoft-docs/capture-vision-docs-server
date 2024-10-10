---
layout: default-layout
title: ImageSourceStateListener Class - Dynamsoft Capture Vision Router Module Python Edition API Reference
description: Definition of ImageSourceStateListener class in Dynamsoft Capture Vision Module Python Edition.
keywords: image source state listener, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# ImageSourceStateListener

Defines a listener for image source state changes.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class ImageSourceStateListener(ABC)
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`on_image_source_state_received`](#on_image_source_state_received) | Called when the state of the image source changes. |

### on_image_source_state_received

This method is called when the state of the image source changes.

```python
@abstractmethod
def on_image_source_state_received(self, state: int) -> None:
```

**Parameters**

`state` The state of the image source. It is one of the values of the `EnumImageSourceState` enumeration.

**See Also**

[EnumImageSourceState]({{ site.dcvb_enumerations }}capture-vision-router/image-source-state.html?lang=python)

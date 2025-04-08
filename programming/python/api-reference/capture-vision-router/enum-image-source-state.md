---
layout: default-layout
title: ImageSourceState - Dynamsoft Vision Router Python Enumerations
description: The enumeration ImageSourceState of Dynamsoft Vision Router describes the state of ImageSourceAdapter.
keywords: Image source state
codeAutoHeight: true
---

# Enumeration ImageSourceState

`ImageSourceState` describes the state of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

```python
class EnumImageSourceState(IntEnum):
    #The buffer of ImageSourceAdapter is temporarily empty.
    ISS_BUFFER_EMPTY
    #The source of ImageSourceAdapter is empty.
    ISS_EXHAUSTED
```
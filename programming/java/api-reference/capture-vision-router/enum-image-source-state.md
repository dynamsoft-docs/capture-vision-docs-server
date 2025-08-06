---
layout: default-layout
title: ImageSourceState - Dynamsoft Vision Router Java Enumerations
description: The enumeration ImageSourceState of Dynamsoft Vision Router describes the state of ImageSourceAdapter.
keywords: Image source state
codeAutoHeight: true
---

# Enumeration ImageSourceState

`ImageSourceState` describes the state of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

```java
@interface EnumImageSourceState {
    //The buffer of ImageSourceAdapter is temporarily empty.
    int ISS_BUFFER_EMPTY = 0;
    //The source of ImageSourceAdapter is empty.
    int ISS_EXHAUSTED = 1;
}
```
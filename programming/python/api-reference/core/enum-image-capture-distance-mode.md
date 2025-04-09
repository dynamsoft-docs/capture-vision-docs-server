---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core Python Enumerations
description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
keywords: Image capture distance
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

```python
class EnumImageCaptureDistanceMode(IntEnum):
   # The image is taken by close-up shot camera.
   ICDM_NEAR
   # The image is taken by long shot camera.
   ICDM_FAR
```

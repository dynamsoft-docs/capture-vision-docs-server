---
layout: default-layout
title: TransformMatrixType - Dynamsoft Core Python Enumerations
description: The enumeration TransformMatrixType of Dynamsoft Core describes transform matrix types.
keywords: Target type
---

# Enumeration TransformMatrixType

`TransformMatrixType` describes the transform matrix types.

```python
class EnumTransformMatrixType(IntEnum):
    # Represents a transformation matrix that converts coordinates from the local image to the original image.
    TMT_LOCAL_TO_ORIGINAL_IMAGE
    # Represents a transformation matrix that converts coordinates from the original image to the local image.
    TMT_ORIGINAL_TO_LOCAL_IMAGE
    # Represents a transformation matrix that converts coordinates from the rotated image to the original image.
    TMT_ROTATED_TO_ORIGINAL_IMAGE
    # Represents a transformation matrix that converts coordinates from the original image to the rotated image.
    TMT_ORIGINAL_TO_ROTATED_IMAGE
```
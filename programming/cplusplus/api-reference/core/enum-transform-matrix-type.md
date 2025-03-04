---
layout: default-layout
title: TransformMatrixType - Dynamsoft Core Enumerations
description: The enumeration TransformMatrixType of Dynamsoft Core describes transform matrix types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TransformMatrixType
---

# Enumeration TransformMatrixType

`TransformMatrixType` describes the transform matrix types.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum TransformMatrixType
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
    TMT_LOCAL_TO_ORIGINAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
    TMT_ORIGINAL_TO_LOCAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
    TMT_ROTATED_TO_ORIGINAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
    TMT_ORIGINAL_TO_ROTATED_IMAGE
    /**Represents a transformation matrix that converts coordinates from the local image to the section image.*/
    TMT_LOCAL_TO_SECTION_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the section image to the local image.*/
    TMT_SECTION_TO_LOCAL_IMAGE
} TransformMatrixType;
```
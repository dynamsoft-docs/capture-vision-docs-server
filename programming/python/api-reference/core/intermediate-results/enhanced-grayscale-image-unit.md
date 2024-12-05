---
layout: default-layout
title: class EnhancedGrayscaleImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class EnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: enhanced grayscale image, python
needAutoGenerateSidebar: true
---

# EnhancedGrayscaleImageUnit

The `EnhancedGrayscaleImageUnit` class represents an intermediate result unit that contains an enhanced grayscale image data. Gray enhancement methods include gray equalization, gray smoothing, gray sharpening and smoothing.

## Definition

*Module:* dynamsoft_core

```python
class EnhancedGrayscaleImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the enhanced grayscale image data. |
| [`set_image_data`](#set_image_data) | Sets the enhanced grayscale image data. |

### get_image_data

Gets the enhanced grayscale image data.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that contains the enhanced grayscale image data.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the enhanced grayscale image data.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

---
layout: default-layout
title: class GrayscaleImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class GrayscaleImageUnit in Dynamsoft Core Module.
keywords: grayscale image, python
needAutoGenerateSidebar: true
---

# GrayscaleImageUnit

The `GrayscaleImageUnit` class represents a grayscale image unit. It is derived from the `IntermediateResultUnit` class.

## Definition

*Module:* dynamsoft_core

```python
class GrayscaleImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the grayscale image. |
| [`set_image_data`](#set_image_data) | Sets the grayscale image. |

### get_image_data

Gets the grayscale image.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that contains the grayscale image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the grayscale image.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.


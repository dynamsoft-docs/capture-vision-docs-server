---
layout: default-layout
title: class BinaryImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class BinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, python
needAutoGenerateSidebar: true
---

# BinaryImageUnit

The `BinaryImageUnit` class represents a unit that contains a binary image. It inherits from the `IntermediateResultUnit` class and stores binary image data.

## Definition

*Module:* dynamsoft_core

```python
class BinaryImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the binary image data. |
| [`set_image_data`](#set_image_data) | Sets the binary image data. |

### get_image_data

Gets the binary image data.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object containing the binary image data.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the binary image data.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

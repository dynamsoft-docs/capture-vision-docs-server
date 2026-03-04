---
layout: default-layout
title: class ScaledColourImageUnit - Dynamsoft Core Module Python Edition API Reference
description: API reference for the ScaledColourImageUnit class in Dynamsoft Core Module Python Edition, which represents an intermediate result unit containing a scaled colour image.
keywords: scaled colour image, python
needAutoGenerateSidebar: true
---

# ScaledColourImageUnit

The `ScaledColourImageUnit` class represents an intermediate result unit that contains scaled  color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Module:* core

```python
class ScaledColourImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the image data of the unit.|
| [`set_image_data`](#set_image_data) | Sets the image data of the unit. |

### get_image_data

Gets the image data of the unit.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that contains the image data of the unit.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the image data of the unit.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

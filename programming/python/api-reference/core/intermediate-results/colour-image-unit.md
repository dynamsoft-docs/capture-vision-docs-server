---
layout: default-layout
title: class ColourImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class ColourImageUnit in Dynamsoft Core Module.
keywords: colour image, python
needAutoGenerateSidebar: true
---

# ColourImageUnit

The `ColourImageUnit` class represents a unit that contains color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Module:* core

```python
class ColourImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the image data of the color image unit. |
| [`set_image_data`](#set_image_data) | Sets the image data of the color image unit. |

### get_image_data

Gets the image data of the color image unit.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that contains the image data of the color image unit.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the image data of the color image unit.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

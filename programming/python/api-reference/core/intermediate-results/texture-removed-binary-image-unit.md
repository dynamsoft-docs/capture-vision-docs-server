---
layout: default-layout
title: class TextureRemovedBinaryImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextureRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: texture removed binary image, python
needAutoGenerateSidebar: true
---

# TextureRemovedBinaryImageUnit

The `TextureRemovedBinaryImageUnit` class represents an intermediate result unit that stores texture-removed binary image data.

## Definition

*Module:* core

```python
class TextureRemovedBinaryImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the texture-removed binary image. |
| [`set_image_data`](#set_image_data) | Sets the texture-removed binary image. |

### get_image_data

Gets the texture-removed binary image.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that represents the texture-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the texture-removed binary image.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

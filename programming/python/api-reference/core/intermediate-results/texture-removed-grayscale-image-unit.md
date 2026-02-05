---
layout: default-layout
title: class TextureRemovedGrayscaleImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: text removed grayscale image, python
needAutoGenerateSidebar: true
---

# TextureRemovedGrayscaleImageUnit

The `TextureRemovedGrayscaleImageUnit` class represents an intermediate result unit that contains texture-removed grayscale image data.

## Definition

*Module:* core

```python
class TextureRemovedGrayscaleImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the texture-removed grayscale image. |
| [`set_image_data`](#set_image_data) | Sets the texture-removed grayscale image. |

### get_image_data

Gets the texture-removed grayscale image.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns a texture-removed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the texture-removed grayscale image.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

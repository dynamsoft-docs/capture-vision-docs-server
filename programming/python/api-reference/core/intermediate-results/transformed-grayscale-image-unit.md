---
layout: default-layout
title: class TransformedGrayscaleImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: transformed grayscale image, python
needAutoGenerateSidebar: true
---

# TransformedGrayscaleImageUnit

The `TransformedGrayscaleImageUnit` class is a subclass of `IntermediateResultUnit` that represents a transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

## Definition

*Module:* core

```python
class TransformedGrayscaleImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the transformed grayscale image.|
| [`set_image_data`](#set_image_data) | Sets the transformed grayscale image. |

### get_image_data

Gets the image data of the transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns a `ImageData` object that represents the image data of the transformed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the transformed grayscale image.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

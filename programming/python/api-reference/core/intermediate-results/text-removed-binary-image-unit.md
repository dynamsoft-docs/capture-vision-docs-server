---
layout: default-layout
title: class TextRemovedBinaryImageUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: text removed binary image, python
needAutoGenerateSidebar: true
---

# TextRemovedBinaryImageUnit

The `TextRemovedBinaryImageUnit` class represents an intermediate result unit that contains a text-removed binary image.

## Definition

*Module:* dynamsoft_core

```python
class TextRemovedBinaryImageUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_image_data`](#get_image_data) | Gets the text-removed binary image. |
| [`set_image_data`](#set_image_data) | Sets the text-removed binary image. |

### get_image_data

Gets the text-removed binary image.

```python
def get_image_data(self) -> ImageData:
```

**Return value**

Returns an `ImageData` object that contains the text-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_image_data

Sets the text-removed binary image.

```python
def set_image_data(self, img_data: ImageData) -> int:
```

**Parameters**

`img_data` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)
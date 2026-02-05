---
layout: default-layout
title: ImageData Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of ImageData class in Dynamsoft Core Module Python Edition.
keywords: image data, python
needAutoGenerateSidebar: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Module:* core

```python
class ImageData
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `ImageData` class. |
| [`get_bytes`](#get_bytes) | Gets the image byte array. |
| [`get_width`](#get_width) | Gets the width of the image. |
| [`get_height`](#get_height) | Gets the height of the image. |
| [`get_stride`](#get_stride) | Gets the stride of the image. |
| [`get_image_pixel_format`](#get_image_pixel_format) | Gets the pixel format of the image. |
| [`get_orientation`](#get_orientation) | Gets the orientation of the image. |
| [`get_image_tag`](#get_image_tag) | Gets the tag of the image. |
| [`set_image_tag`](#set_image_tag) | Sets the tag of the image. |


### \_\_init\_\_

Initializes a new instance of the `ImageData` class

```python
def __init__(self, *args):
```

**Parameters**

`args` <*tuple*>: A variable-length argument list that must contain following parameters in order:

- `bytes` <*bytes*>: The image byte array.
- `width` <*int*>: The width of the image.
- `height` <*int*>: The height of the image.
- `stride` <*int*>: The stride of the image.
- `format` <*int*>: The pixel format of the image.
- `orientation` <*int*, optional>: The orientation of the image.
- `tag` <*ImageTag*, optional>: The tag of the image.

**See Also**

[EnumImagePixelFormat]({{ site.dcvb_python_api }}core/enum-image-pixel-format.html)

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### get_bytes

Gets the image byte array.

```python
def get_bytes(self) -> bytes:
```

**Return Value**

Returns an image byte array.

### get_width

Gets the width of the image.

```python
def get_width(self) -> int:
```

**Return Value**

Returns the width of the image.

### get_height

Gets the height of the image.

```python
def get_height(self) -> int:
```

**Return Value**

Returns the height of the image.

### get_stride

Gets the stride of the image.

```python
def get_stride(self) -> int:
```

**Return Value**

Returns the stride of the image.

### get_image_pixel_format

Gets the pixel format of the image.

```python
def get_image_pixel_format(self) -> int:
```

**Return Value**

Returns the pixel format of the image.

**See Also**

[EnumImagePixelFormat]({{ site.dcvb_python_api }}core/enum-image-pixel-format.html)

### get_orientation

Gets the orientation of the image.

```python
def get_orientation(self) -> int:
```

**Return Value**

Returns the orientation of the image.

### get_image_tag

Gets the tag of the image.

```python
def get_image_tag(self) -> ImageTag:
```

**Return Value**

Returns a tag of the image.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### set_image_tag

Sets the tag of the image.

```python
def set_image_tag(self, tag: ImageTag) -> None:
```

**Parameters**

`tag` The tag of the image.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)


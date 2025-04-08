---
layout: default-layout
title: ImageTag Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of ImageTag class in Dynamsoft Core Module Python Edition.
keywords: image tag, python
needAutoGenerateSidebar: true
---

# ImageTag

The `ImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Module:* dynamsoft_core

```python
class ImageTag(ABC) 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `ImageTag` class. |
| [`get_type`](#get_type) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |
| [`get_image_id`](#get_image_id) | Gets the ID of the image. |
| [`set_image_id`](#set_image_id) | Sets the ID of the image. |
| [`get_image_capture_distance_mode`](#get_image_capture_distance_mode) | Gets the capture distance mode of the image. |
| [`set_image_capture_distance_mode`](#set_image_capture_distance_mode) | Sets the capture distance mode of the image. |

### \_\_init\_\_

Initializes a new instance of the `ImageTag` class.

```python
def __init__(self):
```

### get_type

Gets the type of the image tag.

```python
@abstractmethod
def get_type(self) -> int:
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_python_api }}core/enum-image-tag-type.html?lang=python)

### clone

Creates a copy of the image tag.

```python
@abstractmethod
def clone(self) -> "ImageTag":
```

**Return Value**

Returns a copy of the image tag.

### get_image_id

Gets the ID of the image.

```python
def get_image_id(self) -> int:
```

**Return Value**

Returns the ID of the image.

### set_image_id

Sets the ID of the image.

```python
def set_image_id(self, imgId: int) -> None:
```

**Parameters**

`imgId` The ID of the image.

### get_image_capture_distance_mode

Gets the capture distance mode of the image.

```python
def get_image_capture_distance_mode(self) -> int:
```

**Return Value**

Returns the capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_python_api }}core/enum-image-capture-distance-mode.html?lang=python)

### set_image_capture_distance_mode

Sets the capture distance mode of the image.

```python
def set_image_capture_distance_mode(self, mode: int) -> None:
```

**Parameters**

`mode` The capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_python_api }}core/enum-image-capture-distance-mode.html?lang=python)

---
layout: default-layout
title: CapturedResultBase Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CapturedResultBase class in Dynamsoft Capture Vision Module Python Edition.
keywords: captured result, python
needAutoGenerateSidebar: true
---

# CapturedResultBase

The `CapturedResultBase` class serves as a base class for all captured result types. It is an abstract base class with multiple subclasses, each representing a different type of captured result..

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class CapturedResultBase 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image.|
| [`get_original_image_tag`](#get_original_image_tag) | Gets the tag of the original image.|
| [`get_rotation_transform_matrix`](#get_rotation_transform_matrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`get_error_code`](#get_error_code) | Gets the error code of the capture operation.|
| [`get_error_string`](#get_error_string) | Gets the error message of the capture operation.|

### get_original_image_hash_id

Gets the hash ID of the original image.

```python
def get_original_image_hash_id(self) -> str:
```

**Return Value**

Returns the hash ID of the original image as a string.

### get_original_image_tag

Gets the tag of the original image.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return Value**

Returns an `ImageTag` object containing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### get_rotation_transform_matrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```python
def get_rotation_transform_matrix(self) -> List[float]:
```

**Return Value**

Returns a float list of length 9 which represents a 3x3 rotation matrix.

### get_error_code

Gets the error code of the capture operation.

```python
def get_error_code(self) -> int:
```

**Return Value**

Returns the error code of the capture operation.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

### get_error_string

Gets the error message of the capture operation.

```python
def get_error_string(self) -> str:
```

**Return Value**

Returns the error message of the capture operation as a string.


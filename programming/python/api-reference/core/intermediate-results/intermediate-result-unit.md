---
layout: default-layout
title: class IntermediateResultUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, python
needAutoGenerateSidebar: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Module:* dynamsoft_core

```python
class IntermediateResultUnit 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_hash_id`](#get_hash_id) | Gets the hash ID of the unit.|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image. |
| [`get_original_image_tag`](#get_original_image_tag) | Gets the image tag of the original image. |
| [`get_transform_matrix`](#get_transform_matrix) | Gets the transformation matrix based on [`EnumTransformMatrixType`]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python). |
| [`get_type`](#get_type) | Gets the type of the intermediate result unit. |
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`replace`](#replace) | Replaces the `IntermediateResultUnit` object to the specified `IntermediateResultUnit` object. |
| [`set_hash_id`](#set_hash_id) | Sets the hash ID of the unit. |
| [`set_original_image_hash_id`](#set_original_image_hash_id) | Sets the hash ID of the original image. |
| [`set_original_image_tag`](#set_original_image_tag) | Sets the image tag of the original image. |
| [`set_transform_matrix`](#set_transform_matrix) | Sets the transformation matrix based on [`EnumTransformMatrixType`]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python). |

### get_hash_id

Gets the hash ID of the intermediate result unit.

```python
def get_hash_id(self) -> str:
```

**Return value**

Returns the hash ID of the unit. 

### get_original_image_hash_id

Gets the hash ID of the original image.

```python
def get_original_image_hash_id(self) -> str:
```

**Return value**

Returns the hash ID of the original image.

### get_original_image_tag

Gets the image tag of the original image.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return value**

Returns the image tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### get_transform_matrix

Gets the transformation matrix based on `EnumTransformMatrixType`.

```python
def get_transform_matrix(self, matrix_type: int) -> List[float]:
```

**Parameters**

`matrix_type`: The transform matrix type. This is one of the values of the [EnumTransformMatrixType]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python) enumeration.

**Return value**

A float array which represents the rotation transform matrix.

**See Also**

[EnumTransformMatrixType]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python)

### get_type

Gets the type of the intermediate result unit.

```python
def get_type(self) -> int:
```

**Return value**

Returns the type of the intermediate result unit.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_enumerations }}core/intermediate-result-unit-type.html?lang=python)

### clone

Creates a copy of the intermediate result unit.

```python
def clone(self) -> "IntermediateResultUnit":
```

**Return value**

Returns a copy of the intermediate result unit.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-unit.html)

### replace

Replaces the specified `IntermediateResultUnit` object with the current `IntermediateResultUnit` object.

```python
def replace(self, unit: "IntermediateResultUnit") -> int:
```

**Parameters**

`unit` The `IntermediateResultUnit` object to be replaced.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

### set_hash_id

Sets the hash ID of the intermediate result unit.

```python
def set_hash_id(self, hash_id: str) -> None:
```

**Parameters**

`hash_id` The hash ID to set.

### set_original_image_hash_id

Sets the hash ID of the original image.

```python
def set_original_image_hash_id(self, original_image_hash_id: str) -> None:
```

**Parameters**

`original_image_hash_id` The hash ID to set.

### set_original_image_tag

Sets the image tag of the original image.

```python
def set_original_image_tag(self, tag: ImageTag) -> None:
```

**Parameters**

`tag` The image tag to set.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### set_transform_matrix

Sets the transformation matrix based on `EnumTransformMatrixType`.

```python
def set_transform_matrix(self, matrix_type: int, matrix: List[float]) -> None:
```

**Parameters**

`matrix_type`: The transform matrix type. This is one of the values of the [EnumTransformMatrixType]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python) enumeration.

`matrix` A float array which represents the rotation transform matrix.

**See Also**

[EnumTransformMatrixType]({{site.dcvb_enumerations}}core/transform-matrix-type.html?lang=python)


---
layout: default-layout
title: class ContoursUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class ContoursUnit in Dynamsoft Core Module.
keywords: contours, python
needAutoGenerateSidebar: true
---

# ContoursUnit

The `ContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `IntermediateResultUnit` class.

## Definition

*Module:* dynamsoft_core

```python
class ContoursUnit(IntermediateResultUnit)
```

## Methods

| Method                    | Description |
|---------------------------|---------------------------------------------|
| [`get_contours`](#get_contours) | Gets the contours.  |
| [`set_contours`](#set_contours) | Sets the contours.  |

### get_contours

Gets the contours.

```python
def get_contours(self) -> Tuple[int, List[Contour], List[Vector4]]:
```

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `contours` <*List[Contour]*>: The contours in the unit.
- `hierarchies` <*List[Vector4]*>: The hierarchies of the contours in the unit.

**See Also**

[Contour]({{ site.dcvb_python_api }}core/basic-classes/contour.html)

[Vector4]({{ site.dcvb_python_api }}core/basic-classes/vector4.html)

### set_contours

Sets the contours and hierarchies in the unit.

```python
def set_contours(self, contours: List[Contour], hierarchies: List[Vector4], matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`contours` The contours in the unit.

`hierarchies` The hierarchies in the unit.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[Contour]({{ site.dcvb_python_api }}core/basic-classes/contour.html)

[Vector4]({{ site.dcvb_python_api }}core/basic-classes/vector4.html)

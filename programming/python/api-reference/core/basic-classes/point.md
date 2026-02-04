---
layout: default-layout
title: Point Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of Point class in Dynamsoft Core Module Python Edition.
keywords: point, python
needAutoGenerateSidebar: true
---

# Point

The `Point` class represents a point in 2D space. It contains an array of two integers, which represent the coordinates of the point.

## Definition

*Module:* core

```python
class Point
```

## Properties 

| Property  | Type | Description |
|-----------|------|-------------|
| `x` | *int* | The x-coordinate of the point. |
| `y` | *int* | The y-coordinate of the point. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Point` class. |
| [`distance_to`](#distance_to) | Calculates the distance between the current point and the specified target point. |
| [`transform_coordinates`](#transform_coordinates) | Transforms the coordinates of a point using a given transformation matrix. |

### \_\_init\_\_

Initializes a new instance of the `Point` class.

```python
def __init__(self, *args):
```

**Parameters**

`args` <*tuple*>: A variable-length argument list that must contain following parameters in order:

- `x` <*int*>: The x-coordinate of the point.
- `y` <*int*>: The y-coordinate of the point.


### distance_to

Calculates the distance between the current point and the specified target point.

```python
def distance_to(self, pt: "Point") -> float:
```

**Parameters**

`pt` The target point to which the distance is calculated.

**Return Value**

A value representing the distance between the current point and the specified target point.

### transform_coordinates

Transforms the coordinates of a point using a given transformation matrix.

```python
@staticmethod
def transform_coordinates(original_point: "Point", transformation_matrix: List[float]) -> "Point":
```

**Parameters**

`original_point` The original point to transform.

`transformation_matrix` The transformation matrix to apply to the coordinates.

**Return Value**

Returns a new `Point` object with the transformed coordinates.


---
layout: default-layout
title: Quadrilateral Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of Quadrilateral class in Dynamsoft Core Module Python Edition.
keywords: quadrilateral, python
needAutoGenerateSidebar: true
---

# Quadrilateral

The `Quadrilateral` class represents a quadrilateral shape in 2D space. It contains an array of four Point objects, which represent the vertices of the quadrilateral.

## Definition

*Module:* dynamsoft_core

```python
class Quadrilateral(object) 
```

## Properties
  
| Property  | Type | Description |
|---------- | ---- |-------------|
| `points` | *List\[[Point]({{ site.dcvb_python_api }}core/basic-classes/point.html)\]* | A Point list of length 4 that define the quadrilateral. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Quadrilateral` class with default values. |
| [`contains`](#this) | Determines whether a point is inside the quadrilateral |
| [`get_area`](#this) | Gets the area of the quadrilateral. |


### \_\_init\_\_

Initializes a new instance of the `Quadrilateral` class with default values.

```python
def __init__(self):
```

### contains

Determines whether a point is inside the quadrilateral.

```python
def contains(self, point: "Point") -> bool:
```

**Parameters**

`point` The point to test.

**Return Value**

Returns true if the point inside the quadrilateral, false otherwise.

**See Also**

[Point]({{ site.dcvb_python_api }}core/basic-classes/point.html)

### get_area

Gets the area of the quadrilateral.

```python
def get_area(self) -> int:
```

**Return Value**

RReturns the area of the quadrilateral.


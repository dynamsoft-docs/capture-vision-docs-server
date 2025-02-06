---
layout: default-layout
title: class Contour - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class Contour in Dynamsoft Core Module.
keywords: contour, python
needAutoGenerateSidebar: true
---

# Contour

The `Contour` class represents a contour in 2D space. It contains an array of `Point` objects, which represent the vertices of the contour.

## Definition

*Module:* dynamsoft_core

```python
class Contour 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Contour` class. |
| [`set_points`](#set_points) | Sets the point array. |
| [`get_points`](#get_points) | Gets the point array. |

### \_\_init\_\_

Initializes a new instance of the `Contour` class.

```python
def __init__(self):
```

### set_points

Sets the point array and the points.

```python
def set_points(self, points: List[Point]) -> None:
```

**Parameters**

`points`: The point array.


### get_points

Gets the point array.

```python
def get_points(self) -> List[Point]:
```

**Return Value**

Return the point array.

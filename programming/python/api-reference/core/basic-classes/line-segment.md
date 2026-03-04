---
layout: default-layout
title: class LineSegment - Dynamsoft Core Module Python Edition API Reference
description: API reference for the LineSegment class in Dynamsoft Core Module Python Edition, which represents a line segment defined by two endpoint coordinates.
keywords: line segment, python
---

# LineSegment

The `LineSegment` class represents a line segment in 2D space. It contains two `Point` objects, which represent the start point and end point of the line segment.

## Definition

*Module:* core

```python
class LineSegment 
```

## Properties
  
| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`start_point`](#start_point) | *[Point]({{ site.dcvb_python_api }}core/basic-classes/point.html)* | The start point of the line segment. |
| [`end_point`](#end_point) | *[Point]({{ site.dcvb_python_api }}core/basic-classes/point.html)* | The end point of the line segment. |
| [`id`](#id) | *int* | The ID of the line segment. |

## Methods

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`__init__`](#__init__) | Initializes a new instance of the `LineSegment` class. |

### \_\_init\_\_

Initializes a new instance of the `LineSegment` class.

```python
def __init__(self):
```

---
layout: default-layout
title: class Corner - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class Corner in Dynamsoft Core Module.
keywords: corner, python
needAutoGenerateSidebar: true
---

# Corner

Corner is a structure in an image consisting of two line segments and intersection point. A Corner represents a point at which the image's brightness or color sharply changes.

## Definition

*Module:* dynamsoft_core

```python
class Corner 
```

## Properties
  
| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`type`](#type) | *int* | The type of the corner. This is one of the values of the [EnumCornerType]({{ site.dcvb_python_api }}core/enum-corner-type.html?lang=python) enumeration. |
| [`intersection`](#intersection) | *[Point]({{ site.dcvb_python_api }}core/basic-classes/point.html)* | The intersection point of the corner. |
| [`line1`](#line1) | *[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)* | One of the line connected to the corner. |
| [`line2`](#line2) | *[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)* | One of the line connected to the corner. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Corner` class. |

### \_\_init\_\_

Initializes a new instance of the `Corner` class.

```python
def __init__(self):
```


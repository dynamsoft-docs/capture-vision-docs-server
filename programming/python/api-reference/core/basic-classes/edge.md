---
layout: default-layout
title: class Edge - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class Edge in Dynamsoft Core Module.
keywords: edge, python
needAutoGenerateSidebar: true
---

# Edge

The class `Edge` is a structure composed of two `Corner` points in an image. A `Corner` represents a point at which the image's brightness or color sharply changes. Therefore, a `Edge` is a line segment connecting two such points that have been identified as corners.

## Definition

*Module:* core

```python
class Edge 
```

## Properties
  
| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`start_corner`](#start_corner) | *[Corner]({{ site.dcvb_python_api }}core/basic-classes/corner.html)* | The start corner point of the edge. |
| [`end_corner`](#end_corner) | *[Corner]({{ site.dcvb_python_api }}core/basic-classes/corner.html)* | The end corner point of the edge. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Edge` class. |

### \_\_init\_\_

Initializes a new instance of the `Edge` class.

```python
def __init__(self):
```


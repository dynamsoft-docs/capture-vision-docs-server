---
layout: default-layout
title: class PredetectedRegionElement - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class PredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, python
---

# PredetectedRegionElement

The `PredetectedRegionElement` class represents a region element that has been pre-detected in an image. It is a subclass of the `RegionObjectElement`.

## Definition

*Module:* dynamsoft_core

```python
class PredetectedRegionElement(RegionObjectElement)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `PredetectedRegionElement` class. |
| [`get_mode_name`](#get_mode_name) | Gets the name of the detection mode used to detect this region element. |
| [`set_location`](#set_location)   | Sets the location of the region object element. |
| [`get_label_id`](#get_label_id)     | Gets the label id of the region object element. |
| [`get_label_name`](#get_label_name) | Gets the label name of the region object element. |

### \_\_init\_\_

Initializes a new instance of the `PredetectedRegionElement` class.

```python
def __init__(self):
```

### get_mode_name

Gets the name of the detection mode used to detect this region element.

```python
def get_mode_name(self) -> str:
```

**Return value**

Returns the name of the detection mode used to detect this region element.

### set_location

Set the location of the region object element.

```python
def set_location(self, loc: Quadrilateral) -> int:
```

**Parameters**

`loc` The location of the region object element.

**Return value**

Returns 0 if success, otherwise an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### get_label_id

Gets the label id of the predetected region element.

```python
def get_label_id(self) -> int:
```

**Return value**

Returns the label id of the predetected region element.

### get_label_name

Gets the label name of the predetected region element.

```python
def get_label_name(self) -> str:
```

**Return value**

Returns the label name of the predetected region element.
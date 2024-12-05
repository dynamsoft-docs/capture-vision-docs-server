---
layout: default-layout
title: class PredetectedRegionElement - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class PredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, python
needAutoGenerateSidebar: true
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

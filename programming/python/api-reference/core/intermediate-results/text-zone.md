---
layout: default-layout
title: class TextZone- Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextZone in Dynamsoft Core Module.
keywords: text zones, python
needAutoGenerateSidebar: true
---

# TextZone

The `TextZone` class represents a single text zone.

## Definition

*Module:* core

```python
class TextZone
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `TextZone` class. |
| [`get_location`](#get_location) | Gets the location of the text zone. |
| [`set_location`](#set_location) | Sets the location of the text zone. |
| [`get_char_contours_indices`](#get_char_contours_indices) | Gets the indices of the character contours. |
| [`set_char_contours_indices`](#set_char_contours_indices) | Sets the indices of the character contours. |

### \_\_init\_\_

Initializes a new instance of the `TextZone` class.

```python
def __init__(self, loc: Quadrilateral = None, char_contours_indices: List[int] = None):
```

**Parameters**

`loc` The location of the text zone.

`char_contours_indices` The indices of the character contours.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### get_location

Gets the location of the text zone.

```python
def get_location(self) -> Quadrilateral:
```

**Return Value**

Returns the location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### set_location

Sets the location of the text zone.

```python
def set_location(self, loc: Quadrilateral):
```

**Parameters**

`loc` The location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### get_char_contours_indices

Gets the indices of the character contours.

```python
def get_char_contours_indices(self) -> List[int]:
```

### set_char_contours_indices

Sets the indices of the character contours.

```python
def set_char_contours_indices(self, char_contours_indices: List[int]):
```

**Parameters**

`char_contours_indices` The indices of the character contours.



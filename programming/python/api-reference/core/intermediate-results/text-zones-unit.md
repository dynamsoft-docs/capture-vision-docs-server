---
layout: default-layout
title: class TextZonesUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextZonesUnit in Dynamsoft Core Module.
keywords: text zones, python
needAutoGenerateSidebar: true
---

# TextZonesUnit

The `TextZonesUnit` class represents a unit that contains text zones. It is derived from `IntermediateResultUnit` class and provides methods to retrieve the count and details of text zones.

## Definition

*Module:* core

```python
class TextZonesUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_count`](#get_count) | Gets the number of text zones.|
| [`get_text_zone`](#get_text_zone) | Gets the quadrilateral shape of the text zone at the specified index. |
| [`remove_all_text_zones`](#remove_all_text_zones) | Removes all text zones from the unit. |
| [`remove_text_zone`](#remove_text_zone) | Removes the text zone at the specified index. |
| [`add_text_zone`](#add_text_zone) | Adds a text zone to the unit. |
| [`set_text_zone`](#set_text_zone) | Sets the text zone at the specified index. |

### get_count

Gets the number of text zones in the unit.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of text zones in the unit.

### get_text_zone

Gets the quadrilateral shape of the text zone at the specified index.

```python
def get_text_zone(self, index: int) -> Tuple[int, TextZone]:
```

**Parameters**

`index` The index of the text zone.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `text_zone` <*TextZone*>: The `TextZone` object at the specified index.

**See Also**

[TextZone]({{ site.dcvb_python_api }}core/intermediate-results/text-zone.html)

### remove_all_text_zones

Removes all text zones from the unit.

```python
def remove_all_text_zones(self) -> None:
```

### remove_text_zone

Removes the text zone at the specified index.

```python
def remove_text_zone(self, index: int) -> int:
```

**Parameters**

`index` The index of the text zone to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_python_api }}core/intermediate-results/text-zone.html)

### add_text_zone

Adds a text zone to the unit.

```python
def add_text_zone(self,text_zone: TextZone, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`text_zone` The text zone to add.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_python_api }}core/intermediate-results/text-zone.html)

### set_text_zone

Sets the text zone at the specified index.

```python
def set_text_zone(self, index: int, text_zone: TextZone, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the text zone to set.

`text_zone` The text zone to set.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_python_api }}core/intermediate-results/text-zone.html)


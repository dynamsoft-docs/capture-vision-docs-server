---
layout: default-layout
title: class ShortLinesUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class ShortLinesUnit in Dynamsoft Core Module.
keywords: Short lines, python
needAutoGenerateSidebar: true
---

# ShortLinesUnit

The `ShortLinesUnit` class represents an intermediate result unit that contains the short lines. It is derived from the `IntermediateResultUnit` class.

## Definition

*Module:* core

```python
class ShortLinesUnit(IntermediateResultUnit)
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`get_count`](#get_count) | Gets the number of short lines in the collection. |
| [`get_short_line`](#get_short_line) | Gets the short line at the specified index. |
| [`remove_all_short_lines`](#remove_all_short_lines) | Removes all short lines from the unit. |
| [`remove_short_line`](#remove_short_line) | Removes the short line at the specified index. |
| [`add_short_line`](#add_short_line) | Adds a short line to the unit. |
| [`set_short_line`](#set_short_line) | Sets the short line at the specified index. |

### get_count

Gets the number of short lines in the collection.

```python
def get_count(self) -> int:
```

**Return Value**

Returns the number of short lines in the collection.

### get_short_line

Gets the short line at the specified index.

```python
def get_short_line(self, index: int) -> LineSegment:
```

**Parameters**

`index` The index of the short line to get.

**Return Value**

A `LineSegment` object that represents the short line at the specified index.

**See Also**

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

### remove_all_short_lines

Removes all short lines from the unit.

```python
def remove_all_short_lines(self) -> None:
```

### remove_short_line

Removes the short line at the specified index.

```python
def remove_short_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the short line to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

### add_short_line

Adds a short line to the unit.

```python
def add_short_line(self, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`line` The short line to add.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

### set_short_line

Sets the short line at the specified index.

```python
def set_short_line(self, index: int, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the short line to set.

`line` The short line to set.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

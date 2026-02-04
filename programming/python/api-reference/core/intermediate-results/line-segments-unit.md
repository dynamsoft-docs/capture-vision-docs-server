---
layout: default-layout
title: class LineSegmentsUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class LineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, python
needAutoGenerateSidebar: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `IntermediateResultUnit`.

## Definition

*Module:* core

```python
class LineSegmentsUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_count`](#get_count) | Gets the number of line segments in the collection.|
| [`get_line_segment`](#get_line_segment) | Gets the specified line segment from the collection. |
| [`remove_all_line_segments`](#remove_all_line_segments) | Removes all line segments from the unit. |
| [`remove_line_segment`](#remove_line_segment) | Removes the line segment at the specified index. |
| [`add_line_segment`](#add_line_segment) | Adds a line segment to the unit. |
| [`set_line_segment`](#set_line_segment) | Sets the line segment at the specified index. |

### get_count

Gets the number of line segments in the collection.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of line segments in the collection.

### get_line_segment

Gets the specified line segment from the collection.

```python
def get_line_segment(self, index: int) -> LineSegment:
```

**Parameters**

`index` The index of the line segment to retrieve.

**Return value**

Returns the `LineSegment` object at the specified index or None if error happens.

**See Also**

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

### remove_all_line_segments

Removes all line segments from the unit.

```python
def remove_all_line_segments(self) -> None:
```

### remove_line_segment

Removes the line segment at the specified index.

```python
def remove_line_segment(self, index: int) -> int:
```

**Parameters**

`index` The index of the line segment to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### add_line_segment

Adds a line segment to the unit.

```python
def add_line_segment(self, line : LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`line` The line segment to add.
`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### set_line_segment

Sets the line segment at the specified index.

```python
def set_line_segment(self, index: int, line: LineSegment, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the line segment to set.

`line` The line segment to set.

`matrix_to_original_image` The transform matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

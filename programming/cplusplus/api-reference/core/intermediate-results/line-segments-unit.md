---
layout: default-layout
title: class CLineSegmentsUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, c++
needAutoGenerateSidebar: true
---

# CLineSegmentsUnit

The `CLineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `CIntermediateResultUnit`.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CLineSegmentsUnit: public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of line segments in the collection.|
| [`GetLineSegment`](#getlinesegment) | Gets the specified line segment from the collection. |
| [`operator[]`](#operator) | Gets the line segment at the specified index. |
| [`RemoveAllLineSegments`](#removealllinesegments) | Removes all line segments from the unit. |
| [`RemoveLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`AddLineSegment`](#addlinesegment) | Adds a line segment to the unit. |
| [`SetLineSegment`](#setlinesegment) | Sets the line segment at the specified index. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetCount

Gets the number of line segments in the collection.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of line segments in the collection.

### GetLineSegment

Gets the specified line segment from the collection.

```cpp
virtual const CLineSegment* GetLineSegement(int index) const
```

**Parameters**

`[in] index` The index of the line segment to retrieve.

**Return value**

Returns the `CLineSegment` object at the specified index or NULL if the index is out of range.

**See Also**

[CLineSegment]({{ site.dcvb_cpp_api }}core/basic-structures/line-segment.html)

### operator[]

Gets the line segment at the specified index.

```cpp
virtual const CLineSegment* operator[](int index) const = 0;
```

**Parameters**

`index` The index of the line segment to get.

**Return Value**

A pointer to the `CLineSegment` object that represents the line segment at the specified index.

### RemoveAllLineSegments

Removes all line segments from the unit.

```cpp
virtual void RemoveAllLineSegments() = 0;
```

### RemoveLineSegment

Removes the line segment at the specified index.

```cpp
virtual int RemoveLineSegment(int index) = 0;
```

**Parameters**

index The index of the line segment to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddLineSegment

Adds a line segment to the unit.

```cpp
virtual int AddLineSegment(const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`line` The line segment to add.
`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### SetLineSegment

Sets the line segment at the specified index.

```cpp
virtual int SetLineSegment(int index, const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`index` The index of the line segment to set.

`line` The line segment to set.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

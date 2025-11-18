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

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLineSegmentsUnit

```cpp
class CLineSegmentsUnit : public CIntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of line segments in the collection.|
| [`GetLineSegment`](#getlinesegment) | Gets the specified line segment from the collection. |
| [`operator[]`](#operator) | Gets the line segment at the specified index. |
| [`RemoveAllLineSegments`](#removealllinesegments) | Removes all line segments from the unit. |
| [`RemoveLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`AddLineSegment`](#addlinesegment) | Adds a line segment to the unit. |
| [`SetLineSegment`](#setlinesegment) | Sets the line segment at the specified index. |
| **Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html):** | |
| [`GetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. |
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetType`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagetag) | Sets the tag of the original image. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#retain) | Increases the reference count of the unit. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via `CTransformMatrixType`. |
| [`SetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#settransformmatrix) | Sets the transformation matrix via `CTransformMatrixType`. |

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

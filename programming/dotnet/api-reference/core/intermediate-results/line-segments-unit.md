---
layout: default-layout
title: class LineSegmentsUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class LineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, .NET
needAutoGenerateSidebar: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `IntermediateResultUnit`.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
public class LineSegmentsUnit : IntermediateResultUnit, IEnumerable<LineSegment>
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of line segments in the collection.|
| [`GetLineSegment`](#getlinesegment) | Gets the specified line segment from the collection. |
| [`GetLineSegments`](#getlinesegments) | Gets all line segments from the collection. |
| [`RemoveAllLineSegments`](#removealllinesegments) | Removes all line segments from the unit. |
| [`RemoveLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`AddLineSegment`](#addlinesegment) | Adds a line segment to the unit. |
| [`SetLineSegment`](#setlinesegment) | Sets the line segment at the specified index. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetCount

Gets the number of line segments in the collection.

```csharp
int GetCount()
```

**Return value**

Returns the number of line segments in the collection.

### GetLineSegment

Gets the specified line segment from the collection.

```csharp
LineSegment GetLineSegement(int index)
```

**Parameters**

`[in] index` The index of the line segment to retrieve.

**Return value**

Returns the `LineSegment` object at the specified index or NULL if the index is out of range.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### GetLineSegments

Gets all line segments from the collection.

```csharp
LineSegment[] GetLineSegements()
```

**Return value**

Returns all `LineSegment` objects.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### RemoveAllLineSegments

Removes all line segments from the unit.

```csharp
void RemoveAllLineSegments()
```

### RemoveLineSegment

Removes the line segment at the specified index.

```csharp
int RemoveLineSegment(int index)
```

**Parameters**

`[in] index` The index of the line segment to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddLineSegment

Adds a line segment to the unit.

```csharp
int AddLineSegment(LineSegment lineSegment, double[]? matrixToOriginalImage = null)
```

**Parameters**

`lineSegment` The line segment to add.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### SetLineSegment

Sets the line segment at the specified index.

```csharp
int SetLineSegment(int index, LineSegment lineSegment, double[] matrixToOriginalImage = null)
```

**Parameters**

`index` The index of the line segment to set.

`lineSegment` The line segment to set.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

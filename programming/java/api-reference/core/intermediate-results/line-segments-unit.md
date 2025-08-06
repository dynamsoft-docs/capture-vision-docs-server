---
layout: default-layout
title: class LineSegmentsUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class LineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, java
needAutoGenerateSidebar: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `IntermediateResultUnit`.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

```java
public class LineSegmentsUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getCount`](#getcount) | Gets the number of line segments in the collection.|
| [`getLineSegment`](#getlinesegment) | Gets the specified line segment from the collection. |
| [`getLineSegments`](#getlinesegments) | Gets all line segments from the collection. |
| [`removeAllLineSegments`](#removealllinesegments) | Removes all line segments from the unit. |
| [`removeLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`addLineSegment`](#addlinesegment) | Adds a line segment to the unit. |
| [`setLineSegment`](#setlinesegment) | Sets the line segment at the specified index. |

### getCount

Gets the number of line segments in the collection.

```java
int getCount()
```

**Return value**

Returns the number of line segments in the collection.

### getLineSegment

Gets the specified line segment from the collection.

```java
LineSegment getLineSegment(int index)
```

**Parameters**

`index` The index of the line segment to retrieve.

**Return value**

Returns the `LineSegment` object at the specified index.

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### getLineSegments

Gets all line segments from the collection.

```java
LineSegment[] getLineSegments()
```

**Return value**

Returns all `LineSegment` objects in the collection.

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### removeAllLineSegments

Removes all line segments from the unit.

```java
void removeAllLineSegments()
```

### removeLineSegment

Removes the line segment at the specified index.

```java
void removeLineSegment(int index) throws CoreException
```

**Parameters**

`index` The index of the line segment to remove.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

### addLineSegment

Adds a line segment to the unit.

```java
void addLineSegment(LineSegment line) throws CoreException
void addLineSegment(LineSegment line, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`line` The line segment to add.

`matrixToOriginalImage` The transform matrix to original image.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### setLineSegment

Sets the line segment at the specified index.

```java
void setLineSegment(int index, LineSegment line) throws CoreException
void setLineSegment(int index, LineSegment line, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`index` The index of the line segment to set.

`line` The line segment to set.

`matrixToOriginalImage` The transform matrix to original image.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

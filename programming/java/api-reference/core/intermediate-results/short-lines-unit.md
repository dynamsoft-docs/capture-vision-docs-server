---
layout: default-layout
title: class ShortLinesUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class ShortLinesUnit in Dynamsoft Core Module.
keywords: Short lines, java
needAutoGenerateSidebar: true
---

# ShortLinesUnit

The `ShortLinesUnit` class represents an intermediate result unit that contains the short lines. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

```java
public class ShortLinesUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getCount`](#getcount) | Gets the number of short lines in the collection. |
| [`getShortLine`](#getshortline) | Gets the short line at the specified index. |
| [`getShortLines`](#getshortlines) | Gets all short lines. |
| [`removeAllShortLines`](#removeallshortlines) | Removes all short lines from the unit. |
| [`removeShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`addShortLine`](#addshortline) | Adds a short line to the unit. |
| [`setShortLine`](#setshortline) | Sets the short line at the specified index. |

### getCount

Gets the number of short lines in the collection.

```java
int getCount()
```

**Return Value**

Returns the number of short lines in the collection.

### getShortLine

Gets the short line at the specified index.

```java
LineSegment getShortLine(int index)
```

**Parameters**

`index` The index of the short line to get.

**Return Value**

A `LineSegment` object that represents the short line at the specified index.

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### getShortLines

Gets all short lines.

```java
LineSegment[] getShortLines()
```

**Return Value**

Returns an array of `LineSegment` objects representing all short lines.

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### removeAllShortLines

Removes all short lines from the unit.

```java
void removeAllShortLines()
```

### removeShortLine

Removes the short line at the specified index.

```java
void removeShortLine(int index) throws CoreException
```

**Parameters**

`index` The index of the short line to remove.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

### addShortLine

Adds a short line to the unit.

```java
void addShortLine(LineSegment line) throws CoreException
void addShortLine(LineSegment line, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`line` The short line to add.

`matrixToOriginalImage` The transform matrix to original image. The array length must be 9.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

### setShortLine

Sets the short line at the specified index.

```java
void setShortLine(int index, LineSegment line) throws CoreException
void setShortLine(int index, LineSegment line, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`index` The index of the short line to set.

`line` The short line to set.

`matrixToOriginalImage` The transform matrix to original image. The array length must be 9.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

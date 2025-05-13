---
layout: default-layout
title: class ShortLinesUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ShortLinesUnit in Dynamsoft Core Module.
keywords: Short lines, .NET
needAutoGenerateSidebar: true
---

# ShortLinesUnit

The `ShortLinesUnit` class represents an intermediate result unit that contains the short lines. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:dynamsoft::intermediate_results

*Assembly:DynamsoftCore

```csharp
class ShortLinesUnit : IntermediateResultUnit, IEnumerable<LineSegment>
```

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`GetCount`](#getcount) | Gets the number of short lines in the collection. |
| [`GetShortLine`](#getshortline) | Gets the short line at the specified index. |
| [`GetShortLines`](#getshortlines) | Gets all the short lines. |
| [`RemoveAllShortLines`](#removeallshortlines) | Removes all short lines from the unit. |
| [`RemoveShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`AddShortLine`](#addshortline) | Adds a short line to the unit. |
| [`SetShortLine`](#setshortline) | Sets the short line at the specified index. |

### GetCount

Gets the number of short lines in the collection.

```csharp
int GetCount()
```

**Return Value**

Returns the number of short lines in the collection.

### GetShortLine

Gets the short line at the specified index.

```csharp
LineSegment GetShortLine(int index)
```

**Parameters**

`index` The index of the short line to get.

**Return Value**

The `LineSegment` object that represents the short line at the specified index.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### GetShortLines

Gets all the short lines.

```csharp
LineSegment[] GetShortLines()
```

**Return Value**

The `LineSegment` object array.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### RemoveAllShortLines

Removes all short lines from the unit.

```csharp
void RemoveAllShortLines()
```

### RemoveShortLine

Removes the short line at the specified index.

```csharp
int RemoveShortLine(int index)
```

**Parameters**

`index` The index of the short line to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddShortLine

Adds a short line to the unit.

```csharp
AddShortLine(LineSegment lineSegment, double[] matrixToOriginalImage = null)
```

**Parameters**

`lineSegment` The short line to add.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### SetShortLine

Sets the short line at the specified index.

```csharp
int SetShortLine(int index, LineSegment lineSegment, double[] matrixToOriginalImage = null)
```

**Parameters**

`index` The index of the short line to set.

`lineSegment` The short line to set.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

---
layout: default-layout
title: class Contour - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class Contour in Dynamsoft Core Module.
keywords: contour, .NET
needAutoGenerateSidebar: true
---

# Contour

The `Contour` class represents a contour in 2D space. It contains an array of `Point` objects, which represent the vertices of the contour.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
class Contour 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetPointsCount`](#getpointscount) | Gets the number of points in the point array. |
| [`GetPoints`](#getpoints) | Gets the point array. |
| [`SetPoints`](#setpoints) | Sets the point array and the points free function pointer. |

### GetPointsCount

Gets the number of points in the point array.

```csharp
int GetPointsCount()
```

**Return Value**

The number of points in the point array.

### GetPoints

Gets the point array.

```csharp
Point[] GetPoints()
```

**Return Value**

Return the point array.

### SetPoints

Sets the point array and the points free function pointer.

```csharp
void SetPoints(Point[] points)
```

**Parameters**

`[in] points`: The point array.

---
layout: default-layout
title: Point Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of Point class in Dynamsoft Core Module .NET Edition.
keywords: point, .NET
needAutoGenerateSidebar: true
---

# Point

The `Point` class represents a point in 2D space. It contains an array of two integers, which represent the coordinates of the point.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
public class Point
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Point`](#point) | Constructor of a `Point` object. |
| [`This`](#this) | Gets or sets the coordinate value at the specified index. |
| [`Set`](#set) | Sets the coordinates of a point. |
| [`DistanceTo`](#distanceto) | Calculates the distance between the current point and the specified target point. |
| [`TransformCoordinates`](#transformcoordinates) | Transforms the coordinates of a point using a given transformation matrix. |

### Point

Initializes a new instance of the `Point` class with default coordinates (0, 0).

```csharp
Point()
```

Initializes a new instance of the `Point` class by copying coordinates from another point.

```csharp
Point(Point other)
```

Initializes a new instance of the `Point` class with the specified coordinates.

```csharp
Point(int x, int y)
```

**Parameters**

`[in] other` The point from which to copy coordinates.

`[in] x` The x-coordinate of the point.

`[in] y` The y-coordinate of the point.


### This

Gets or sets the coordinate value at the specified index.

```csharp
int this[int index]
```

**Parameters**

`[in] index` The index of the coordinate value to get or set. Index 0 corresponds to the x-coordinate, and index 1 corresponds to the y-coordinate.

**Return Value**

Returns the value of the coordinate at the specified index.

### Set

Sets the coordinates of a point.

```csharp
void Set(int x, int y)
```

**Parameters**

`[in] x` The new x-coordinate of a point.

`[in] y` The new y-coordinate of a point.

### DistanceTo

Calculates the distance between the current point and the specified target point.

```csharp
double DistanceTo(Point pt)
```

**Parameters**

`[in] pt` The target point to which the distance is calculated.

**Return Value**

A value representing the distance between the current point and the specified target point.

### TransformCoordinates

Transforms the coordinates of a point using a given transformation matrix.

```csharp
static Point TransformCoordinates(Point originalPoint, double transformationMatrix[9])
```

**Parameters**

`[in] originalPoint` The original point to transform.

`[in] transformationMatrix` The transformation matrix to apply to the coordinates.

**Return Value**

Returns a new `Point` object with the transformed coordinates.


---
layout: default-layout
title: class CPoint - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPoint in Dynamsoft Core Module.
keywords: point, c++
needAutoGenerateSidebar: true
---

# CPoint

The `CPoint` class represents a point in 2D space. It contains an array of two integers, which represent the coordinates of the point.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
typedef DMPoint_<int> CPoint;
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`Set`](#set) | Sets the coordinates of a point. |
| [`operator[]`](#operator) | Gets the element at the specified index in the `CPoint`. |
| [`DistanceTo`](#distanceto) | Calculates the distance between the current point and the specified target point. |
| [`TransformCoordinates`](#transformcoordinates) | Transforms the coordinates of a point using a given transformation matrix. |

### Set

Sets the coordinates of a point.

```cpp
void Set(int x, int y)
```

**Parameters**

`[in] x` The x coordinate of a point.

`[in] y` The y coordinate of a point.

### operator[]

Gets the element at the specified index in the `CPoint`.

```cpp
int& operator[](int i)
```

**Parameters**

`[in] i` An integer index used to access the element of the `CPoint`.

**Return Value**

A reference to the element at the specified index in the `CPoint`.

### DistanceTo

Calculates the distance between the current point and the specified target point.

```cpp
double DistanceTo(const CPoint& pt) const;
```

**Parameters**

`[in] pt` The target point to which the distance is calculated.

**Return Value**

A floating-point value representing the distance between the current point and the specified target point.

### TransformCoordinates

Transforms the coordinates of a point using a given transformation matrix.

```cpp
static CPoint TransformCoordinates(CPoint originalPoint, double transformationMatrix[9])
```

**Parameters**

`[in] originalPoint` The original point to transform.

`[in] transformationMatrix` The transformation matrix to apply to the coordinates.

**Return value**

Returns a new `CPoint` object with the transformed coordinates.

**Code Snippet**

```cpp
CPoint originalPoint;
originalPoint.Set(10, 20);

double transformationMatrix[9] = {1, 0, 0, 0, 2, 0, 0, 0, 1};

CPoint transformedPoint = CPoint::TransformCoordinates(originalPoint, transformationMatrix);
```

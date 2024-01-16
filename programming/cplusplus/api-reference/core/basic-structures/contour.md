---
layout: default-layout
title: class CContour - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CContour in Dynamsoft Core Module.
keywords: contour, c++
needAutoGenerateSidebar: true
---

# CContour

The `CContour` class represents a contour in 2D space. It contains an array of CPoint objects, which represent the vertices of the contour.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CContour 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`SetPoints`](#setpoints) | Sets the point array and the points free function pointer. |
| [`GetPointsCount`](#getpointscount) | Gets the number of points in the point array. |
| [`GetPoints`](#getpoints) | Gets the point array. |
| [`~CContour`](#ccontour-destructor) | The destructor of CContour. |

### ~CContour Destructor

The destructor of CContour. It releases the memory of the point array.

```cpp
~CContour()
```

### SetPoints

Sets the point array and the points free function pointer.

```cpp
void SetPoints(int pointsCount, const CPoint* points, FreePointsFunc freePointsFunc);
```

**Parameters**

`[in] pointsCount`: The number of points in the point array.

`[in] points`: The point array.

`[in] freePointsFunc`: The freePointsFunc function pointer.

### GetPointsCount

Gets the number of points in the point array.

```cpp
int GetPointsCount() const;
```

**Return Value**

The number of points in the point array.

### GetPoints

Gets the point array.

```cpp
const CPoint* GetPoints() const;
```

**Return Value**

Return the point array.

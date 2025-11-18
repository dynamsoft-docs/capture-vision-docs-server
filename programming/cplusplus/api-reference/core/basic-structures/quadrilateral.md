---
layout: default-layout
title: class CQuadrilateral - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CQuadrilateral in Dynamsoft Core Module.
keywords: quadrilateral, c++
needAutoGenerateSidebar: true
---

# CQuadrilateral

The `CQuadrilateral` class represents a quadrilateral shape in 2D space. It contains an array of four CPoint objects, which represent the vertices of the quadrilateral.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CQuadrilateral 
```

## Attributes Summary
  
| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *CPoint* |
| [`id`](#id) | *int* |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Contains`](#contains) | Determines whether a point is inside the quadrilateral.|
| [`GetArea`](#getarea) | Gets the area of the quadrilateral. |
| [`GetBoundingRect`](#getboundingrect) | Gets the bounding rectangle of the quadrilateral. |

### points

The point array of the quadrilateral.

```cpp
CPoint points[4]
```

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)

### id

The id of the quadrilateral.

```cpp
int id
```

### Contains

Determines whether a point is inside the quadrilateral.

```cpp
bool Contains(const CPoint* point) const
```

**Parameters**

`[in] point` The point to test.

**Return value**

Returns true if the point inside the quadrilateral, false otherwise. 

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)

### GetArea

Gets the area of the quadrilateral.

```cpp
int GetArea() const
```

**Return value**

Returns the area of the quadrilateral.

### GetBoundingRect

Gets the bounding rectangle of the quadrilateral.

```cpp
CRect GetBoundingRect() const;
```

**Return value**

Returns the bounding rectangle of the quadrilateral, in type of `CRect`.
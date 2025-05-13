---
layout: default-layout
title: Quadrilateral Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of Quadrilateral class in Dynamsoft Core Module .NET Edition.
keywords: quadrilateral, .NET
needAutoGenerateSidebar: true
---

# Quadrilateral

The `Quadrilateral` class represents a quadrilateral shape in 2D space. It contains an array of four Point objects, which represent the vertices of the quadrilateral.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
public class Quadrilateral 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *Point* |
| [`id`](#points) | *int* |

### points

The array of points that define the quadrilateral.

```csharp
Point[] points
```

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### id

The id of the quadrilateral.

```csharp
int id
```


## Methods

| Method               | Description |
|----------------------|-------------|
| [`Quadrilateral`](#quadrilateral) | Initializes a new instance of the `Quadrilateral` class with default values. |
| [`Contains`](#contains) | Determines whether a point is inside the quadrilateral.|
| [`GetArea`](#getarea) | Gets the area of the quadrilateral. |
| [`GetBoundingRect`](#getboundingrect) | Gets the bounding rectangle of the quadrilateral. |
| [`this`](#this) | Gets or sets the point at the specified index in the quadrilateral. |


### Quadrilateral

Initializes a new instance of the `Quadrilateral` class with default values.

```csharp
Quadrilateral()
```

### Contains

Determines whether a point is inside the quadrilateral.

```csharp
bool Contains(Point pt)
```

**Parameters**

`[in] pt` The point to test.

**Return value**

Returns true if the point inside the quadrilateral, false otherwise. 

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### GetArea

Gets the area of the quadrilateral.

```csharp
int GetArea()
```

**Return value**

Returns the area of the quadrilateral.

### GetBoundingRect

Gets the bounding rectangle of the quadrilateral.

```csharp
Rect GetBoundingRect()
```

**Return value**

Returns the bounding rectangle of the quadrilateral, in type of `Rect`.

**See Also**

[Rect]({{ site.dcvb_dotnet_api }}core/basic-classes/rect.html)

### This

Gets or sets the point at the specified index in the quadrilateral.

```csharp
Point this[int index]
```

**Parameters**

`[in] index` The index of the point to get or set.

**Return Value**

Returns the point at the specified index.

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

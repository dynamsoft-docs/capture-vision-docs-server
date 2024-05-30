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

*Assembly:* Dynamsoft.Core.dll

```csharp
public class Quadrilateral 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *Point* |

### points

The array of points that define the quadrilateral.

```csharp
Point[] points;
```

**See Also**

[Point]({{ site.dcv_dotnet_api }}core/basic-classes/point.html)

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Quadrilateral`](#quadrilateral) | Initializes a new instance of the `Quadrilateral` class with default values. |
| [`this`](#this) | Gets or sets the point at the specified index in the quadrilateral. |


### Quadrilateral

Initializes a new instance of the `Quadrilateral` class with default values.

```csharp
Quadrilateral()
```

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

[Point]({{ site.dcv_dotnet_api }}core/basic-classes/point.html)

---
layout: default-layout
title: class Corner - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class Corner in Dynamsoft Core Module.
keywords: corner, .NET
needAutoGenerateSidebar: true
---

# Corner

`Corner` is a structure in an image consisting of two line segments and intersection point. A `Corner` represents a point at which the image's brightness or color sharply changes.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
class Corner
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`type`](#type) | *EnumCornerType* |
| [`intersection`](#intersection) | *Point* |
| [`line1`](#line1) | *LineSegment* |
| [`line2`](#line2) | *LineSegment* |

### type

The type of the corner.

```csharp
EnumCornerType type
```

**See Also**

[EnumCornerType]({{ site.dcvb_dotnet_api }}core/enum-corner-type.html)

### intersection

The intersection point of the corner.

```csharp
Point intersection
```

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### line1

One of the line connected to the corner.

```csharp
LineSegment line1
```

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

### line2

One of the line connected to the corner.

```csharp
LineSegment line2
```

**See Also**

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

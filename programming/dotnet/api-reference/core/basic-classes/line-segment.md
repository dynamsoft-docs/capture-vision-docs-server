---
layout: default-layout
title: class LineSegment - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class LineSegment in Dynamsoft Core Module.
keywords: line segment, .NET
needAutoGenerateSidebar: true
---

# LineSegment

The `LineSegment` class represents a line segment in 2D space. It contains two `Point` objects, which represent the start point and end point of the line segment.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
class LineSegment 
```

## Methods Summary

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`GetStartPoint`](#getstartpoint) | Gets the start point of the line segment. |
| [`GetEndPoint`](#getendpoint) | Gets the end point of the line segment. |
| [`SetStartPoint`](#setstartpoint) | Sets the start point of the line segment. |
| [`SetEndPoint`](#setendpoint) | Sets the end point of the line segment. |
| [`GetId`](#getid) | Gets the id of the line segment. |
| [`SetId`](#setid) | Sets the id of the line segment. |

### GetStartPoint

Gets the start point of the line segment.

```csharp
Point  GetStartPoint()
```

**Return Value**

Returns the start point of the line segment.

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### GetEndPoint

Gets the end point of the line segment.

```csharp
Point  GetEndPoint()
```

**Return Value**

Returns the end point of the line segment.

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### SetStartPoint

Sets the start point of the line segment.

```csharp
void SetStartPoint(Point pt)
```

**Parameters**

`[in] pt`: The start point of the line segment.

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### SetEndPoint

Sets the end point of the line segment.

```csharp
void SetEndPoint(Point pt)
```

**Parameters**

`[in] pt`: The end point of the line segment.

**See Also**

[Point]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)

### GetId

Gets the id of the line segment.

```csharp
int GetId();
```

**Return Value**

Returns the id of the line segment.

### SetId

Sets the id of the line segment.

```csharp
void SetId(int lineId);
```

**Parameters**

`[in] lineId`: The id of the line segment.

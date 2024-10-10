---
layout: default-layout
title: class CLineSegment - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLineSegment in Dynamsoft Core Module.
keywords: line segment, c++
needAutoGenerateSidebar: true
---

# CLineSegment

The `CLineSegment` class represents a line segment in 2D space. It contains two CPoint objects, which represent the start point and end point of the line segment.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CLineSegment 
```

## Methods Summary

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`GetStartPoint`](#getstartpoint) | Gets the start point of the line segment. |
| [`GetEndPoint`](#getendpoint) | Gets the end point of the line segment. |
| [`SetStartPoint`](#setstartpoint) | Sets the start point of the line segment. |
| [`SetEndPoint`](#setendpoint) | Sets the end point of the line segment. |

### GetStartPoint

Gets the start point of the line segment.

```cpp
const CPoint&  GetStartPoint() const
```

**Return Value**

Returns the start point of the line segment.

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)

### GetEndPoint

Gets the end point of the line segment.

```cpp
const CPoint&  GetEndPoint() const
```

**Return Value**

Returns the end point of the line segment.

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)

### SetStartPoint

Sets the start point of the line segment.

```cpp
void SetStartPoint(const CPoint& pt)
```

**Parameters**

`[in] pt`: The start point of the line segment.

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)

### SetEndPoint

Sets the end point of the line segment.

```cpp
void SetEndPoint(const CPoint& pt)
```

**Parameters**

`[in] pt`: The end point of the line segment.

**See Also**

[CPoint]({{ site.dcvb_cpp_api }}core/basic-structures/point.html)


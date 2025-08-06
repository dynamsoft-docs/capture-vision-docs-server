---
layout: default-layout
title: class LineSegment - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class LineSegment in Dynamsoft Core Module.
keywords: line segment, java
---

# LineSegment

The `LineSegment` class represents a line segment in 2D space. It contains two `Point` objects, which represent the start point and end point of the line segment.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class LineSegment
```

## Constructors

| Constructor                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`LineSegment()`](#linesegment) | Initializes a new instance of the `LineSegment` class. |
| [`LineSegment(Point start, Point end)`](#linesegment-1) | Initializes a new instance with start and end points. |
| [`LineSegment(Point start, Point end, int lineId)`](#linesegment-2) | Initializes a new instance with start point, end point, and line ID. |
| [`LineSegment(LineSegment line)`](#linesegment-3) | Copy constructor. |

## Methods

| Method | Description |
|--------|-------------|
| [`getStartPoint`](#getstartpoint) | Gets the start point of the line segment. |
| [`getEndPoint`](#getendpoint) | Gets the end point of the line segment. |
| [`setStartPoint`](#setstartpoint) | Sets the start point of the line segment. |
| [`setEndPoint`](#setendpoint) | Sets the end point of the line segment. |
| [`getId`](#getid) | Gets the ID of the line segment. |
| [`setId`](#setid) | Sets the ID of the line segment. |

## Constructors

### LineSegment

Initializes a new instance of the `LineSegment` class.

```java
LineSegment()
```

### LineSegment

Initializes a new instance of the `LineSegment` class with start and end points.

```java
LineSegment(Point start, Point end)
```

**Parameters**

`start` The start point of the line segment.

`end` The end point of the line segment.

### LineSegment

Initializes a new instance of the `LineSegment` class with start point, end point, and line ID.

```java
LineSegment(Point start, Point end, int lineId)
```

**Parameters**

`start` The start point of the line segment.

`end` The end point of the line segment.

`lineId` The ID of the line segment.

### LineSegment

Copy constructor. Initializes a new instance of the `LineSegment` class by copying another LineSegment.

```java
LineSegment(LineSegment line)
```

**Parameters**

`line` The LineSegment object to copy.

## Methods

### getStartPoint

Gets the start point of the line segment.

```java
Point getStartPoint()
```

**Return Value**

Returns the start point of the line segment.

**See Also**

[Point]({{ site.dcvb_java_api }}core/basic-classes/point.html)

### getEndPoint

Gets the end point of the line segment.

```java
Point getEndPoint()
```

**Return Value**

Returns the end point of the line segment.

**See Also**

[Point]({{ site.dcvb_java_api }}core/basic-classes/point.html)

### setStartPoint

Sets the start point of the line segment.

```java
void setStartPoint(Point point)
```

**Parameters**

`point` The start point to set.

### setEndPoint

Sets the end point of the line segment.

```java
void setEndPoint(Point point)
```

**Parameters**

`point` The end point to set.

### getId

Gets the ID of the line segment.

```java
int getId()
```

**Return Value**

Returns the ID of the line segment.

### setId

Sets the ID of the line segment.

```java
void setId(int lineId)
```

**Parameters**

`lineId` The ID to set for the line segment.

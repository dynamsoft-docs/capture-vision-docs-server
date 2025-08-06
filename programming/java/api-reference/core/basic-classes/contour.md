---
layout: default-layout
title: class Contour - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class Contour in Dynamsoft Core Module.
keywords: contour, java
needAutoGenerateSidebar: true
---

# Contour

The `Contour` class represents a contour in 2D space. It contains an array of `Point` objects, which represent the vertices of the contour.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class Contour
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Contour()`](#contour) | Initializes a new instance of the `Contour` class. |
| [`Contour(Contour contour)`](#contour-1) | Initializes a new instance of the `Contour` class with another contour. |
| [`setPoints`](#setpoints) | Sets the point array. |
| [`getPoints`](#getpoints) | Gets the point array. |

### Contour()

Initializes a new instance of the `Contour` class.

```java
public Contour()
```

### Contour(Contour contour)

Initializes a new instance of the `Contour` class with another contour.

```java
public Contour(Contour contour)
```

**Parameters**

`contour`: Another contour object to copy from.

### setPoints

Sets the point array.

```java
public void setPoints(Point[] points)
```

**Parameters**

`points`: The point array.

### getPoints

Gets the point array.

```java
public Point[] getPoints()
```

**Return Value**

Returns the point array.

**See Also**

[Point]({{ site.dcvb_java_api }}core/basic-classes/point.html)

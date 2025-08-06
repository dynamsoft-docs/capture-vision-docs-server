---
layout: default-layout
title: Point Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of Point class in Dynamsoft Core Module Java Edition.
keywords: point, java
needAutoGenerateSidebar: true
---

# Point

The `Point` class represents a point in 2D space. It contains an array of two integers, which represent the coordinates of the point.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class Point
```

## Properties 

| Property  | Type | Description |
|-----------|------|-------------|
| `x` | *int* | The x-coordinate of the point. |
| `y` | *int* | The y-coordinate of the point. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Point`](#point) | Initializes a new instance of the `Point` class. |
| [`getX`](#getx) | Gets the x-coordinate of the point. |
| [`getY`](#gety) | Gets the y-coordinate of the point. |
| [`distanceTo`](#distanceto) | Calculates the distance between the current point and the specified target point. |
| [`transformCoordinate`](#transformcoordinate) | Transforms the coordinates of a point using a given transformation matrix. |

### Point

Initializes a new instance of the `Point` class.

```java
public Point()
public Point(int x, int y)
public Point(Point pt)
```

**Parameters**

`x` The x-coordinate of the point.

`y` The y-coordinate of the point.

`pt` Another Point object to copy from.

### getX

Gets the x-coordinate of the point.

```java
public int getX()
```

**Return Value**

Returns the x-coordinate of the point.

### getY

Gets the y-coordinate of the point.

```java
public int getY()
```

**Return Value**

Returns the y-coordinate of the point.

### distanceTo

Calculates the distance between the current point and the specified target point.

```java
public double distanceTo(Point pt)
```

**Parameters**

`pt` The target point to which the distance is calculated.

**Return Value**

A value representing the distance between the current point and the specified target point.

### transformCoordinate

Transforms the coordinates of a point using a given transformation matrix.

```java
public static Point transformCoordinate(Point originalPoint, double[] transformationMatrix)
```

**Parameters**

`originalPoint` The original point to transform.

`transformationMatrix` The transformation matrix to apply to the coordinates.

**Return Value**

Returns a new `Point` object with the transformed coordinates.

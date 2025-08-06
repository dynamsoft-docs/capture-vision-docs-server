---
layout: default-layout
title: Quadrilateral Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of Quadrilateral class in Dynamsoft Core Module Java Edition.
keywords: quadrilateral, java
---

# Quadrilateral

The `Quadrilateral` class represents a quadrilateral shape in 2D space. It contains an array of four Point objects, which represent the vertices of the quadrilateral.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class Quadrilateral
```

## Attributes
  
| Attribute  | Type | Description |
|---------- | ---- |-------------|
| [`points`](#points) | *Point[]* | An array of 4 Points that define the quadrilateral. |
| [`id`](#id) | *int* | The ID of the quadrilateral. |

## Constructors

| Constructor | Description |
|-------------|-------------|
| [`Quadrilateral()`](#quadrilateral) | Default constructor. Initializes a new instance of the `Quadrilateral` class. |
| [`Quadrilateral(Quadrilateral quadrilateral)`](#quadrilateral-1) | Copy constructor. |
| [`Quadrilateral(Point point1, Point point2, Point point3, Point point4)`](#quadrilateral-2) | Initializes with four points. |
| [`Quadrilateral(Point point1, Point point2, Point point3, Point point4, int id)`](#quadrilateral-3) | Initializes with four points and an ID. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`contains`](#contains) | Determines whether a point is inside the quadrilateral |
| [`getArea`](#getarea) | Gets the area of the quadrilateral. |
| [`getBoundingRect`](#getboundingrect) | Gets the bounding rectangle of the quadrilateral. |

## Attributes

### points

An array of 4 Points that define the quadrilateral.

```java
public Point[] points
```

### id

The ID of the quadrilateral.

```java
public int id
```

## Constructors

### Quadrilateral

Default constructor. Initializes a new instance of the `Quadrilateral` class with default values.

```java
Quadrilateral()
```

### Quadrilateral

Copy constructor. Initializes a new instance by copying another Quadrilateral.

```java
Quadrilateral(Quadrilateral quadrilateral)
```

**Parameters**

`quadrilateral` The Quadrilateral object to copy.

### Quadrilateral

Initializes a new instance with four points.

```java
Quadrilateral(Point point1, Point point2, Point point3, Point point4)
```

**Parameters**

`point1` The first point of the quadrilateral.

`point2` The second point of the quadrilateral.

`point3` The third point of the quadrilateral.

`point4` The fourth point of the quadrilateral.

### Quadrilateral

Initializes a new instance with four points and an ID.

```java
Quadrilateral(Point point1, Point point2, Point point3, Point point4, int id)
```

**Parameters**

`point1` The first point of the quadrilateral.

`point2` The second point of the quadrilateral.

`point3` The third point of the quadrilateral.

`point4` The fourth point of the quadrilateral.

`id` The ID of the quadrilateral.

## Methods

### contains

Determines whether a point is inside the quadrilateral.

```java
boolean contains(Point point)
```

**Parameters**

`point` The point to test.

**Return Value**

Returns true if the point inside the quadrilateral, false otherwise.

**See Also**

[Point]({{ site.dcvb_java_api }}core/basic-classes/point.html)

### getArea

Gets the area of the quadrilateral.

```java
int getArea()
```

**Return Value**

Returns the area of the quadrilateral.

### getBoundingRect

Gets the bounding rectangle of the quadrilateral.

```java
Rect getBoundingRect()
```

**Return Value**

Returns bounding rectangle of the quadrilateral, in type of [`Rect`]({{ site.dcvb_java_api }}core/basic-classes/rect.html).


---
layout: default-layout
title: class Corner - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class Corner in Dynamsoft Core Module.
keywords: corner, java
needAutoGenerateSidebar: true
---

# Corner

Corner is a structure in an image consisting of two line segments and intersection point. A Corner represents a point at which the image's brightness or color sharply changes.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class Corner
```

## Attributes
  
| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`type`](#type) | *int* | The type of the corner. This is one of the values of the [EnumCornerType]({{ site.dcvb_java_api }}core/enum-corner-type.html) enumeration. |
| [`intersection`](#intersection) | *[Point]({{ site.dcvb_java_api }}core/basic-classes/point.html)* | The intersection point of the corner. |
| [`line1`](#line1) | *[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)* | One of the line connected to the corner. |
| [`line2`](#line2) | *[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)* | One of the line connected to the corner. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Corner()`](#corner) | Initializes a new instance of the `Corner` class. |
| [`Corner(Corner corner)`](#corner-1) | Initializes a new instance of the `Corner` class with another corner. |

### Corner()

Initializes a new instance of the `Corner` class.

```java
public Corner()
```

### Corner(Corner corner)

Initializes a new instance of the `Corner` class with another corner.

```java
public Corner(Corner corner)
```

**Parameters**

`corner`: Another corner object to copy from.

### type

The type of the corner.

```java
public @EnumCornerType int type
```

### intersection

The intersection point of the corner.

```java
public Point intersection
```

### line1

One of the line segments connected to the corner.

```java
public LineSegment line1
```

### line2

One of the line segments connected to the corner.

```java
public LineSegment line2
```


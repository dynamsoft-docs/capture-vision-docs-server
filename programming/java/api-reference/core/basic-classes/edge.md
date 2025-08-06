---
layout: default-layout
title: class Edge - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class Edge in Dynamsoft Core Module.
keywords: edge, java
needAutoGenerateSidebar: true
---

# Edge

The class `Edge` is a structure composed of two `Corner` points in an image. A `Corner` represents a point at which the image's brightness or color sharply changes. Therefore, a `Edge` is a line segment connecting two such points that have been identified as corners.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class Edge
```

## Attributes
  
| Attribute | Type | Description |
|---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)* | The start corner point of the edge. |
| [`endCorner`](#endcorner) | *[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)* | The end corner point of the edge. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`Edge()`](#edge) | Initializes a new instance of the `Edge` class. |
| [`Edge(Edge edge)`](#edge-1) | Initializes a new instance of the `Edge` class with another edge. |

### Edge()

Initializes a new instance of the `Edge` class.

```java
public Edge()
```

### Edge(Edge edge)

Initializes a new instance of the `Edge` class with another edge.

```java
public Edge(Edge edge)
```

**Parameters**

`edge`: Another edge object to copy from.

### startCorner

The start corner point of the edge.

```java
public Corner startCorner
```

### endCorner

The end corner point of the edge.

```java
public Corner endCorner
```


---
layout: default-layout
title: Rect Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of Rect class in Dynamsoft Core Module Java Edition.
keywords: rect, java
---

# Rect

The `Rect` class represents a rectangle in 2D space. It contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class Rect
```

## Attributes

| Attribute  | Type | Description |
|---------- | ---- |-------------|
| [`top`](#top) | *int* | The top edge of the rectangle. |
| [`left`](#left) | *int* | The left edge of the rectangle. |
| [`right`](#right) | *int* | The right edge of the rectangle. |
| [`bottom`](#bottom) | *int* | The bottom edge of the rectangle. |
| [`id`](#id) | *int* | The ID of the rectangle. |

## Constructors

| Constructor | Description |
|-------------|-------------|
| [`Rect()`](#rect) | Default constructor. Initializes a new instance of the `Rect` class. |
| [`Rect(int top, int left, int right, int bottom)`](#rect-1) | Initializes a new instance with specified coordinates. |
| [`Rect(Rect rect)`](#rect-2) | Copy constructor. |

## Attributes

### top

The top edge of the rectangle.

```java
public int top
```

### left

The left edge of the rectangle.

```java
public int left
```

### right

The right edge of the rectangle.

```java
public int right
```

### bottom

The bottom edge of the rectangle.

```java
public int bottom
```

### id

The ID of the rectangle.

```java
public int id
```

## Constructors

### Rect

Default constructor. Initializes a new instance of the `Rect` class.

```java
Rect()
```

### Rect

Initializes a new instance of the `Rect` class with specified coordinates.

```java
Rect(int top, int left, int right, int bottom)
```

**Parameters**

`top` The top edge of the rectangle.

`left` The left edge of the rectangle.

`right` The right edge of the rectangle.

`bottom` The bottom edge of the rectangle.

### Rect

Copy constructor. Initializes a new instance of the `Rect` class by copying another Rect.

```java
Rect(Rect rect)
```

**Parameters**

`rect` The Rect object to copy.


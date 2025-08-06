---
layout: default-layout
title: class Vector4 - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class Vector4 in Dynamsoft Core Module.
keywords: vector4, java
needAutoGenerateSidebar: true
---

# Vector4

The `Vector4` class represents a four-dimensional vector.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class Vector4
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`value`](#value) | *int[]* | An array of 4 integers representing the vector components. |

## Constructors

| Constructor | Description |
|-------------|-------------|
| [`Vector4()`](#vector4) | Default constructor. Initializes a new instance of the `Vector4` class. |
| [`Vector4(Vector4 v)`](#vector4-1) | Copy constructor. |
| [`Vector4(int v1, int v2, int v3, int v4)`](#vector4-2) | Initializes a new instance with specific values. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`set`](#set) | Sets the components value of the four-dimensional vector. |
| [`getItems`](#getitems) | Gets the component values as an array. |

## Attributes

### value

An array of 4 integers representing the vector components.

```java
public int[] value
```

## Constructors

### Vector4

Default constructor. Initializes a new instance of the `Vector4` class.

```java
Vector4()
```

### Vector4

Copy constructor. Initializes a new instance by copying another Vector4.

```java
Vector4(Vector4 v)
```

**Parameters**

`v` The Vector4 object to copy.

### Vector4

Initializes a new instance of the `Vector4` class with specific values.

```java
Vector4(int v1, int v2, int v3, int v4)
```

**Parameters**

`v1` The first component value.

`v2` The second component value.

`v3` The third component value.

`v4` The fourth component value.

## Methods

### set

Sets the components value of the four-dimensional vector.

```java
void set(int v1, int v2, int v3, int v4)
```

**Parameters**

`v1` The first component value.

`v2` The second component value.

`v3` The third component value.

`v4` The fourth component value.

### getItems

Gets the component values as an array.

```java
int[] getItems()
```

**Return Value**

Returns an array containing the four component values of the vector.

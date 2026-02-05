---
layout: default-layout
title: class TextZone- Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TextZone in Dynamsoft Core Module.
keywords: text zones, java
needAutoGenerateSidebar: true
---

# TextZone

The `TextZone` class represents a single text zone.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextZone
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`TextZone`](#textzone) | Initializes a new instance of the `TextZone` class. |
| [`getLocation`](#getlocation) | Gets the location of the text zone. |
| [`setLocation`](#setlocation) | Sets the location of the text zone. |
| [`getCharContoursIndices`](#getcharcontoursindices) | Gets the indices of the character contours. |
| [`setCharContoursIndices`](#setcharcontoursindices) | Sets the indices of the character contours. |

### TextZone

Initializes a new instance of the `TextZone` class.

```java
TextZone()
TextZone(Quadrilateral loc)
TextZone(Quadrilateral loc, int[] charContoursIndices)
TextZone(TextZone textZone)
```

**Parameters**

`loc` The location of the text zone.

`charContoursIndices` The indices of the character contours.

`textZone` Another TextZone object to copy from.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getLocation

Gets the location of the text zone.

```java
Quadrilateral getLocation()
```

**Return Value**

Returns the location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### setLocation

Sets the location of the text zone.

```java
void setLocation(Quadrilateral loc)
```

**Parameters**

`loc` The location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getCharContoursIndices

Gets the indices of the character contours.

```java
int[] getCharContoursIndices()
```

**Return Value**

Returns an array of integers representing the indices of the character contours.

### setCharContoursIndices

Sets the indices of the character contours.

```java
void setCharContoursIndices(int[] charContoursIndices)
```

**Parameters**

`charContoursIndices` The indices of the character contours.



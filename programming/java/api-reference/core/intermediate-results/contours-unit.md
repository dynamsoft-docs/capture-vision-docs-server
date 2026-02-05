---
layout: default-layout
title: class ContoursUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class ContoursUnit in Dynamsoft Core Module.
keywords: contours, java
needAutoGenerateSidebar: true
---

# ContoursUnit

The `ContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class ContoursUnit extends IntermediateResultUnit
```

## Methods

| Method                    | Description |
|---------------------------|---------------------------------------------|
| [`getContours`](#getcontours) | Gets the contours.  |
| [`getHierarchies`](#gethierarchies) | Gets the hierarchies.  |
| [`setContours`](#setcontours) | Sets the contours.  |

### getContours

Gets the contours.

```java
Contour[] getContours() throws CoreException
```

**Return value**

Returns the contours in the unit.

**See Also**

[Contour]({{ site.dcvb_java_api }}core/basic-classes/contour.html)

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

### getHierarchies

Gets the hierarchies.

```java
Vector4[] getHierarchies() throws CoreException
```

**Return value**

Returns the hierarchies of the contours in the unit.

**See Also**

[Vector4]({{ site.dcvb_java_api }}core/basic-classes/vector4.html)

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

### setContours

Sets the contours and hierarchies in the unit.

```java
void setContours(Contour[] contours, Vector4[] hierarchies) throws CoreException
void setContours(Contour[] contours, Vector4[] hierarchies, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`contours` The contours in the unit.

`hierarchies` The hierarchies in the unit.

`matrixToOriginalImage` The transform matrix to original image.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[Contour]({{ site.dcvb_java_api }}core/basic-classes/contour.html)

[Vector4]({{ site.dcvb_java_api }}core/basic-classes/vector4.html)

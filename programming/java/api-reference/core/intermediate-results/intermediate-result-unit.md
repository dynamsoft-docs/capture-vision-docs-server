---
layout: default-layout
title: class IntermediateResultUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, java
---

# IntermediateResultUnit

The `IntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Package:* `com.dynamsoft.core.intermediate_results`

```java
class IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getHashId`](#gethashid) | Gets the hash ID of the unit.|
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the original image. |
| [`getTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix based on [`EnumTransformMatrixType`]({{ site.dcvb_java_api }}core/enum-transform-matrix-type.html). |
| [`getType`](#gettype) | Gets the type of the intermediate result unit. |
| [`getUsageCount`](#getusagecount) | Gets the usage count of the intermediate result. |
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`replace`](#replace) | Replaces the `IntermediateResultUnit` object to the specified `IntermediateResultUnit` object. |

### getHashId

Gets the hash ID of the intermediate result unit.

```java
String getHashId()
```

**Return value**

Returns the hash ID of the unit. 

### getOriginalImageHashId

Gets the hash ID of the original image.

```java
String getOriginalImageHashId()
```

**Return value**

Returns the hash ID of the original image.

### getOriginalImageTag

Gets the image tag of the original image.

```java
ImageTag getOriginalImageTag()
```

**Return value**

Returns the image tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### getTransformMatrix

Gets the transformation matrix based on `EnumTransformMatrixType`.

```java
double[] getTransformMatrix(@EnumTransformMatrixType int matrixType)
```

**Parameters**

`matrixType` The transform matrix type. This is one of the values of the [EnumTransformMatrixType]({{ site.dcvb_java_api }}core/enum-transform-matrix-type.html) enumeration.

**Return value**

A double array which represents the rotation transform matrix.

**See Also**

[EnumTransformMatrixType]({{ site.dcvb_java_api }}core/enum-transform-matrix-type.html)

### getType

Gets the type of the intermediate result unit.

```java
@EnumIntermediateResultUnitType long getType()
```

**Return value**

Returns the type of the intermediate result unit.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_java_api }}core/enum-intermediate-result-unit-type.html)

### getUsageCount

Gets the usage count of the intermediate result.

```java
int getUsageCount()
```

**Return value**

Returns the usage count of the intermediate result.

### clone

Creates a copy of the intermediate result unit.

```java
IntermediateResultUnit clone()
```

**Return value**

Returns a copy of the intermediate result unit.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html)

### replace

Replaces the specified `IntermediateResultUnit` object with the current `IntermediateResultUnit` object.

```java
void replace(IntermediateResultUnit unit) throws CoreException
```

**Parameters**

`unit` The `IntermediateResultUnit` object to be replaced.

**Exceptions**

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/exceptions/core-exception.html)


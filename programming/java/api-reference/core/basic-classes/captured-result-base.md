---
layout: default-layout
title: CapturedResultBase Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CapturedResultBase class in Dynamsoft Capture Vision Module Java Edition.
keywords: captured result, java
needAutoGenerateSidebar: true
---

# CapturedResultBase

The `CapturedResultBase` class serves as a base class for all captured result types. It is an abstract base class with multiple subclasses, each representing a different type of captured result..

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class CapturedResultBase 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image.|
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image.|
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`getErrorCode`](#geterrorcode) | Gets the error code of the capture operation.|
| [`getErrorString`](#geterrorstring) | Gets the error message of the capture operation.|

### getOriginalImageHashId

Gets the hash ID of the original image.

```java
public String getOriginalImageHashId()
```

**Return Value**

Returns the hash ID of the original image as a string.

### getOriginalImageTag

Gets the tag of the original image.

```java
public ImageTag getOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object containing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### getRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```java
public double[] getRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### getErrorCode

Gets the error code of the capture operation.

```java
public int getErrorCode()
```

**Return Value**

Returns the error code of the capture operation.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### getErrorString

Gets the error message of the capture operation.

```java
public String getErrorString()
```

**Return Value**

Returns the error message of the capture operation as a string.


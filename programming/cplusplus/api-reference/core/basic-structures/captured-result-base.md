---
layout: default-layout
title: class CCapturedResultBase - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultBase in Dynamsoft Core Module.
keywords: captured result base, c++
needAutoGenerateSidebar: true
---

# CCapturedResultBase

The CCapturedResultBase class serves as a base class for all captured result types. It is an abstract base class with multiple subclasses, each representing a different type of captured result.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CCapturedResultBase 
```

## Methods Summary

| Method                         | Description|
|--------------------------------|------------|
| [`~CCapturedResultBase`](#ccapturedresultbase-destructor) | This is the class destructor. |
| [`GetOriginalImageHashId`](#getoriginalimagehashid)| Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag)| Gets the tag of the original image. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix)| Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`GetErrorCode`](#geterrorcode)| Gets the error code of the detection operation. |
| [`GetErrorString`](#geterrorstring)| Gets the error message of the detection operation. |

### CCapturedResultBase Destructor

This is the class destructor.

```cpp
virtual ~CCapturedResultBase(){};
```

### GetOriginalImageHashId

Gets the hash ID of the original image.

```cpp
virtual const char* GetOriginalImageHashId()const = 0;
```

**Return value**

Returns a pointer to a null-terminated string that represents the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```cpp
virtual const CImageTag* GetOriginalImageTag()const = 0;
```

**Return value**

Returns a pointer to a `CImageTag` object that represents the tag of the original image.

**See Also**

[CImageTag]({{ site.dcvb_cpp_api }}core/basic-structures/image-tag.html)

### GetRotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```cpp
virtual void GetRotationTransformMatrix(double matrix[9]) const = 0;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.

### GetErrorCode

Gets the error code of the detection operation.

```cpp
virtual int GetErrorCode()const = 0;
```

**Return value**

Returns the error code.

**See Also**

[ErrorCode]({{ site.dcvb_cpp_api }}core/enum-error-code.html)

### GetErrorString

Gets the error message of the detection operation.

```cpp
virtual const char* GetErrorString()const = 0;
```

**Return value**

Returns a pointer to a null-terminated string that represents the error message.
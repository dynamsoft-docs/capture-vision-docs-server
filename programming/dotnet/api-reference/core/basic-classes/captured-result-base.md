---
layout: default-layout
title: class CapturedResultBase - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class CapturedResultBase in Dynamsoft Core Module.
keywords: captured result base, .NET
needAutoGenerateSidebar: true
---

# CapturedResultBase

The `CapturedResultBase` class serves as a base class for all captured result types. It is an abstract base class with multiple subclasses, each representing a different type of captured result.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
public abstract class CapturedResultBase : IDisposable
```

## Methods Summary

| Method                         | Description|
|--------------------------------|------------|
| [`GetOriginalImageHashId`](#getoriginalimagehashid)| Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag)| Gets the tag of the original image. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix)| Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`GetErrorCode`](#geterrorcode)| Gets the error code of the detection operation. |
| [`GetErrorString`](#geterrorstring)| Gets the error message of the detection operation. |

### GetOriginalImageHashId

Gets the hash ID of the original image.

```csharp
string GetOriginalImageHashId()
```

**Return value**

Returns a null-terminated string that represents the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```csharp
ImageTag GetOriginalImageTag()
```

**Return value**

Returns an `ImageTag` object that represents the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)

### GetRotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```csharp
double[] GetRotationTransformMatrix()
```

**Return value**

Returns a double array which represents the rotation transform matrix.

### GetErrorCode

Gets the error code of the detection operation.

```csharp
int GetErrorCode()
```

**Return value**

Returns the error code.

**See Also**

[ErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### GetErrorString

Gets the error message of the detection operation.

```csharp
string GetErrorString()
```

**Return value**

Returns a null-terminated string that represents the error message.
---
layout: default-layout
title: class IntermediateResultUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class IntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, .NET
needAutoGenerateSidebar: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class IntermediateResultUnit : IDisposable 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetHashId`](#gethashid) | Gets the hash ID of the unit.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the original image. |
| [`GetIntermediateResultUnitType`](#getintermediateresultunittype) | Gets the type of the intermediate result unit. |
| [`Clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`GetTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.dcvb_dotnet_api }}core/enum-transform-matrix-type.html). |
| [`Replace`](#replace) | Replaces the `IntermediateResultUnit` object to the specified `IntermediateResultUnit` object. |
| [`GetUsageCount`](#getusagecount)|Gets the usage count of the intermediate result.|

### GetHashId

Gets the hash ID of the intermediate result unit.

```csharp
string GetHashId()
```

**Return value**

Returns the hash ID of the unit. 

### GetOriginalImageHashId

Gets the hash ID of the original image.

```csharp
string GetOriginalImageHashId()
```

**Return value**

Returns the hash ID of the original image.

### GetOriginalImageTag

Gets the image tag of the original image.

```csharp
ImageTag GetOriginalImageTag()
```

**Return value**

Returns the image tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)

### GetIntermediateResultUnitType

Gets the type of the intermediate result unit.

```csharp
EnumIntermediateResultUnitType GetIntermediateResultUnitType()
```

**Return value**

Returns the type of the intermediate result unit.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### Clone

Creates a copy of the intermediate result unit.

```csharp
virtual IntermediateResultUnit Clone()
```

**Return value**

Returns a copy of the intermediate result unit.

### GetTransformMatrix

Gets the transformation matrix via `EnumTransformMatrixType`.

```csharp
double[] GetTransformMatrix(EnumTransformMatrixType matrixType)
```

**Parameters**

`[in] matrixType`: The transform matrix type.

The corresponding transformation matrices are as follows:

- local image to original image
- original image to local image
- rotated image to original image
- original image to rotated image

**Return value**

A double array which represents the rotation transform matrix.

**See Also**

[EnumTransformMatrixType]({{site.dcvb_dotnet_api }}core/enum-transform-matrix-type.html)

### Replace

Replaces the specified `IntermediateResultUnit` object with the current `IntermediateResultUnit` object.

```csharp
int Replace(IntermediateResultUnit unit)
```

**Parameters**

`unit` The `IntermediateResultUnit` object to be replaced.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

### GetUsageCount

Gets the usage count of the intermediate result.

```csharp
int GetUsageCount();
```

**Return value**

Returns the usage count of the intermediate result.


---
layout: default-layout
title: class CIntermediateResultUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultUnit in Dynamsoft Core Module.
keywords: intermediate result, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultUnit

The `CIntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CIntermediateResultUnit 
```


## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetHashId`](#gethashid) | Gets the hash ID of the unit.|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the original image. |
| [`GetType`](#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`](#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`](#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`](#setoriginalimagetag) | Sets the image tag of the original image. |
| [`Retain`](#retain) | Increases the reference count of the unit. |
| [`Release`](#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`TransformMatrixType`]({{site.dcvb_cpp_api}}core/enum-transform-matrix-type.html?src=cpp&&lang=cpp). |
| [`SetTransformMatrix`](#settransformmatrix) | Sets the transformation matrix via [`TransformMatrixType`]({{site.dcvb_cpp_api}}core/enum-transform-matrix-type.html?src=cpp&&lang=cpp). |
| [`Replace`](#replace) | Replaces the `CIntermediateResultUnit` object to the specified `CIntermediateResultUnit` object. |
| [`GetUsageCount`](#getusagecount)|Gets the usage count of the intermediate result.|
| [`SetUsageCount`](#setusagecount)|Sets the usage count of the intermediate result.|

### GetHashId

Gets the hash ID of the intermediate result unit.

```cpp
const char* GetHashId() const
```

**Return value**

Returns the hash ID of the unit. 

### GetOriginalImageHashId

Gets the hash ID of the original image.

```cpp
const char* GetOriginalImageHashId() const
```

**Return value**

Returns the hash ID of the original image.

### GetOriginalImageTag

Gets the image tag of the original image.

```cpp
const CImageTag* GetOriginalImageTag() const
```

**Return value**

Returns the image tag of the original image.

**See Also**

[CImageTag]({{ site.dcvb_cpp_api }}core/basic-structures/image-tag.html)

### GetType

Gets the type of the intermediate result unit.

```cpp
virtual IntermediateResultUnitType GetType() const = 0
```

**Return value**

Returns the type of the intermediate result unit.

**See Also**

[IntermediateResultUnitType]({{ site.dcvb_cpp_api }}core/enum-intermediate-result-unit-type.html?src=cpp&&lang=cpp)

### Clone

Creates a copy of the intermediate result unit.

```cpp
virtual CIntermediateResultUnit* Clone() const = 0
```

**Return value**

Returns a copy of the intermediate result unit.

**See Also**

[CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html)

### SetHashId

Sets the hash ID of the intermediate result unit.

```cpp
void SetHashId(const char* _hashId)
```

**Parameters**

`[in] _hashId` The hash ID to set.

### SetOriginalImageHashId

Sets the hash ID of the original image.

```cpp
void SetOriginalImageHashId(const char* _originalImageHashId)
```

**Parameters**

`[in] _originalImageHashId` The hash ID to set.

### SetOriginalImageTag

Sets the image tag of the original image.

```cpp
void SetOriginalImageTag(const CImageTag* _tag)
```

**Parameters**

`[in] _tag` The image tag to set.

**See Also**

[CImageTag]({{ site.dcvb_cpp_api }}core/basic-structures/image-tag.html)

### Retain

Increases the reference count of the intermediate result unit.

```cpp
virtual CIntermediateResultUnit* Retain() = 0
```

**Return value**

Returns an object of the `CIntermediateResultUnit` class.

### Release

Decreases the reference count of the intermediate result unit.

```cpp
virtual void Release() = 0
```

### GetTransformMatrix

Gets the transformation matrix via `TransformMatrixType`.

```cpp
void GetTransformMatrix(TransformMatrixType matrixType, double matrix[9]) const;
```

**Parameters**

`[in] matrixType`: The transform matrix type.

`[out] matrix` A double array which represents the rotation transform matrix.

The corresponding transformation matrices are as follows:

- local image to original image
- original image to local image
- rotated image to original image
- original image to rotated image

**See Also**

[TransformMatrixType]({{site.dcvb_cpp_api}}core/enum-transform-matrix-type.html?src=cpp&&lang=cpp)

### SetTransformMatrix

Sets the transformation matrix via `TransformMatrixType`.

```cpp
void SetTransformMatrix(TransformMatrixType matrixType, double matrix[9]);
```

**Parameters**

`[in] matrixType`: The transform matrix type.

`[in] matrix` A double array which represents the rotation transform matrix.

The corresponding transformation matrices are as follows:

- local image to original image
- original image to local image
- rotated image to original image
- original image to rotated image

**See Also**

[TransformMatrixType]({{site.dcvb_cpp_api}}core/enum-transform-matrix-type.html?src=cpp&&lang=cpp)

### Replace

Replaces the specified `CIntermediateResultUnit` object with the current `CIntermediateResultUnit` object.

```cpp
virtual int Replace(CIntermediateResultUnit* unit) = 0;
```

**Parameters**

`unit` The `CIntermediateResultUnit` object to be replaced.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

### GetUsageCount

Gets the usage count of the intermediate result.

```cpp
int GetUsageCount() const;
```

**Return value**

Returns the usage count of the intermediate result.

### SetUsageCount

Sets the usage count of the intermediate result.

```cpp
void SetUsageCount(int usageCount)
```

**Parameters**

`[in] _usageCount` The usage count of the intermediate result.
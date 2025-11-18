---
layout: default-layout
title: class CTextureDetectionResultUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, c++
needAutoGenerateSidebar: true
---

# CTextureDetectionResultUnit

The `CTextureDetectionResultUnit` class represents an intermediate result unit for texture detection. It is derived from the `CIntermediateResultUnit` class and contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CTextureDetectionResultUnit

```cpp
class CTextureDetectionResultUnit : public CIntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetXSpacing`](#getxspacing) | Gets x-direction spacing of the texture stripes. |
| [`GetYSpacing`](#getyspacing) | Gets y-direction spacing of the texture stripes. |
| [`SetXSpacing`](#setxspacing) | Sets x-direction spacing of the texture stripes. |
| [`SetYSpacing`](#setyspacing) | Sets y-direction spacing of the texture stripes. |
| **Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html):** | |
| [`GetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. |
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetType`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagetag) | Sets the tag of the original image. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#retain) | Increases the reference count of the unit. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via `CTransformMatrixType`. |
| [`SetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#settransformmatrix) | Sets the transformation matrix via `CTransformMatrixType`. |

### GetXSpacing

Gets x-direction spacing of the texture stripes.

```cpp
virtual int GetXSpacing() 
```

**Return value**

Returns the x-direction spacing of the texture stripes.

### GetYSpacing

Gets y-direction spacing of the texture stripes.

```cpp
virtual int GetYSpacing() 
```

**Return value**

Returns the y-direction spacing of the texture stripes.

### SetXSpacing

Sets the x-direction spacing of the texture stripes.

```cpp
virtual void SetXSpacing(int xSpacing) = 0;
```

**Parameters**

`[in] xSpacing` The x-direction spacing of the texture stripes.

### SetYSpacing

Sets the y-direction spacing of the texture stripes.

```cpp
virtual void SetYSpacing(int ySpacing) = 0;
```

**Parameters**

`[in] ySpacing` The y-direction spacing of the texture stripes.

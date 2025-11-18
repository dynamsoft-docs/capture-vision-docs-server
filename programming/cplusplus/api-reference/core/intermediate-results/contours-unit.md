---
layout: default-layout
title: class CContoursUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CContoursUnit in Dynamsoft Core Module.
keywords: contours, c++
needAutoGenerateSidebar: true
---

# CContoursUnit

The `CContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CContoursUnit

```cpp
class CContoursUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method                    | Description |
|---------------------------|---------------------------------------------|
| [`GetContours`](#getcontours) | Gets the contours.  |
| [`SetContours`](#setcontours) | Sets the contours.  |
| **Inherited Methods from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html):** | |
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

### GetContours

Gets the contours.

```cpp
virtual int GetContours(int* count, const CContour** contours, const CVector4** hierarchies) const;
```

**Parameters**

`[out] count` The count of contours in the unit.

`[out] contours` The contours in the unit.

`[out] hierarchies` The hierarchies of the contours in the unit.

**Return value**

Returns 0 if successful, or an error code if the contour could not be retrieved.

**See Also**

[CContour]({{ site.dcvb_cpp_api }}core/basic-structures/contour.html)

[CVector4]({{ site.dcvb_cpp_api }}core/basic-structures/vector4.html)

### SetContours

Sets the contours and hierarchies in the unit.

```cpp
virtual int SetContours(int count, const CContour* contours, const CVector4* hierarchies, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] count` The number of contours in the unit.

`[in] contours` The contours in the unit.

`[in] hierarchies` The hierarchies in the unit.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

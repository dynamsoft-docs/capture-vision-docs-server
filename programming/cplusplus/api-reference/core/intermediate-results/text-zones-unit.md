---
layout: default-layout
title: class CTextZonesUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextZonesUnit in Dynamsoft Core Module.
keywords: text zones, c++
needAutoGenerateSidebar: true
---

# CTextZonesUnit

The `CTextZonesUnit` class represents a unit that contains text zones. It is derived from `CIntermediateResultUnit` class and provides methods to retrieve the count and details of text zones.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CTextZonesUnit

```cpp
class CTextZonesUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of text zones.|
| [`GetTextZone`](#gettextzone) | Gets the quadrilateral shape of the text zone at the specified index. |
| [`RemoveAllTextZones`](#removealltextzones) | Removes all text zones from the unit. |
| [`RemoveTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`AddTextZone`](#addtextzone) | Adds a text zone to the unit. |
| [`SetTextZone`](#settextzone) | Sets the text zone at the specified index. |
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

### GetCount

Gets the number of text zones in the unit.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of text zones in the unit.

### GetTextZone

Gets the quadrilateral shape of the text zone at the specified index.

```cpp
virtual int GetTextZone(int index, CTextZone* textZone) const = 0;
```

**Parameters**

`[in] index` The index of the text zone.

`[in, out] textZone` A pointer to a CTextZone object to receive  the text zone.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### RemoveAllTextZones

Removes all text zones from the unit.

```cpp
virtual void RemoveAllTextZones() = 0;
```

### RemoveTextZone

Removes the text zone at the specified index.

```cpp
virtual int RemoveTextZone(int index) = 0;
```

**Parameters**

index The index of the text zone to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddTextZone

Adds a text zone to the unit.

```cpp
virtual int AddTextZone(const CTextZone& textZone, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] textZone` The text zone to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### SetTextZone

Sets the text zone at the specified index.

```cpp
virtual int SetTextZone(int index, const CTextZone& textZone, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the text zone to set.

`[in] textZone` The text zone to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

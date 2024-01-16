---
layout: default-layout
title: class CPredetectedRegionsUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, c++
needAutoGenerateSidebar: true
---

# CPredetectedRegionsUnit

The `CPredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions. It inherits from the `CIntermediateResultUnit` class and stores the result of image color pre-detection.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CPredetectedRegionsUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of pre-detected regions in the collection. |
| [`GetPredetectedRegion`](#getpredetectedregion) | Gets a pointer to a specific pre-detected region in the collection. |
| [`operator[]`](#operator) | Gets a pointer to a specific pre-detected region in the collection. |
| [`RemoveAllPredetectedRegions`](#removeallpredetectedregions) | Removes all pre-detected regions in the unit. |
| [`RemovePredetectedRegion`](#removepredetectedregion) | Removes a pre-detected region in the unit at the specified index. |
| [`AddPredetectedRegion`](#addpredetectedregion) | Adds a pre-detected region in the unit. |
| [`SetPredetectedRegion`](#setpredetectedregion) | Sets a pre-detected region in the unit at the specified index. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetCount

Gets the number of pre-detected regions in the collection.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of pre-detected regions in the collection.

### GetPredetectedRegion

Gets a pointer to a specific pre-detected region in the collection.

```cpp
virtual const CPredetectedRegionElement* GetPredetectedRegion(int index) const
```

**Parameters**

`[in] index` The index of the pre-detected region to retrieve.

**Return value**

Returns a const pointer to the specified pre-detected region in the collection. You don't need to release the memory pointed to by the returned pointer.

**See Also**

[CPredetectedRegionElement]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)

### operator[]

Gets a pointer to a specific pre-detected region in the collection.

```cpp
virtual const CPredetectedRegionElement* operator[](int index) const = 0;
```

**Parameters** 

`[in] index` The index of the pre-detected region to retrieve.

**Return Value**

Returns a const pointer to the specified pre-detected region in the collection. You don't need to release the memory pointed to by the returned pointer.

### RemoveAllPredetectedRegions

Removes all pre-detected regions in the unit.

```cpp
virtual void RemoveAllPredetectedRegions() = 0;
```

### RemovePredetectedRegion

Removes a pre-detected region in the unit at the specified index.

```cpp
virtual int RemovePredetectedRegion(int index) = 0;
```

**Parameters**

`[in] index` The index of the pre-detected region to remove.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

### AddPredetectedRegion

Adds a pre-detected region in the unit.

```cpp
virtual int AddPredetectedRegion(const CPredetectedRegionElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The pre-detected region to add.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

### SetPredetectedRegion

Sets a pre-detected region in the unit at the specified index.

```cpp
virtual int SetPredetectedRegion(int index, const CPredetectedRegionElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters** 

`[in] index` The index of the pre-detected region to set.
`[in] element` The pre-detected region to set.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

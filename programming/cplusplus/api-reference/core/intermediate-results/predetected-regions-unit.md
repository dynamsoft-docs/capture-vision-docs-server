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

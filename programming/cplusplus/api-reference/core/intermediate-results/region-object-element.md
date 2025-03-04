---
layout: default-layout
title: class CRegionObjectElement - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CRegionObjectElement in Dynamsoft Core Module.
keywords: region object element, c++
needAutoGenerateSidebar: true
---

# CRegionObjectElement

The `CRegionObjectElement` class represents an element of a region object in 2D space. It is an abstract class that provides the interface for region object elements.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CRegionObjectElement 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetLocation`](#getlocation) | Get the location of the region object element. |
| [`GetReferencedElement`](#getreferencedelement) | Get a pointer to a referenced region object element. |
| [`GetElementType`](#getelementtype) | Get the type of the region object element. |
| [`GetImageData`](#getimagedata) | Get the imageData of the region object element. |
| [`Clone`](#clone) | Clone the region object element. |
| [`Retain`](#retain) | Increases the reference count of the `CRegionObjectElement` object. |
| [`Release`](#release) | Decreases the reference count of the `CRegionObjectElement` object. |

### GetLocation

Get the location of the region object element.

```cpp
CQuadrilateral GetLocation() const
```

**Return value**

Returns a `CQuadrilateral` object which represents the location of the region object element.

**See Also**

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### GetReferencedElement

Get a pointer to a referenced region object element.

```cpp
const CRegionObjectElement* GetReferencedElement() const
```

**Return value**

Returns a const pointer to a referenced `CRegionObjectElement` object.

**See Also**

[CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html)

### GetElementType

Get the type of the region object element.

```cpp
RegionObjectElementType GetElementType() const
```

**Return value**

Returns a `RegionObjectElementType` enum value which represents the type of the region object element.

**See Also**

[RegionObjectElementType]({{ site.dcvb_cpp_api }}core/enum-region-object-element-type.html?src=cpp&&lang=cpp)

### GetImageData

Get the imageData of the region object element.

```cpp
const CImageData* GetImageData() const;
```

**Return value**

Returns a const pointer to a referenced `CImageData` object.

### Clone

Clone the region object element.

```cpp
virtual CRegionObjectElement* Clone() const = 0;
```

**Return value**

Returns a pointer to a copy of the region object element.

### Retain

Increases the reference count of the `CRegionObjectElement` object.

```cpp
virtual CRegionObjectElement* Retain() = 0;
```

**Return value**

An object of `CRegionObjectElement`.

### Release

Decreases the reference count of the `CRegionObjectElement` object.

```cpp
virtual void Release() = 0;
```

---
layout: default-layout
title: class CAuxiliaryRegionElement - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CAuxiliaryRegionElement in Dynamsoft Core Module.
keywords: auxiliary region element, c++
---

# CAuxiliaryRegionElement

The `CAuxiliaryRegionElement` class represents an auxiliary region element that contains additional region information detected during processing (e.g., MRZ, portrait zones, signature areas). It inherits from the `CRegionObjectElement` class.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CAuxiliaryRegionElement

```cpp
class CAuxiliaryRegionElement : public CRegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetName`](#getname) | Gets the name of this auxiliary region. |
| [`GetConfidence`](#getconfidence) | Gets the confidence level of this auxiliary region detection. |
| [`SetName`](#setname) | Sets the name of this auxiliary region. |
| [`SetLocation`](#setlocation) | Sets the location of this auxiliary region. |
| [`SetConfidence`](#setconfidence) | Sets the confidence level of this auxiliary region detection. |
| **Methods Inherited from [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html):** | |
| [`GetLocation`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object element. |
| [`GetReferencedElement`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets a pointer to a referenced region object element. |
| [`GetElementType`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getelementtype) | Gets the type of the region object element. |
| [`GetImageData`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the imageData of the region object element. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#clone) | Clone the region object element. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#retain) | Increases the reference count of the `CRegionObjectElement` object. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#release) | Decreases the reference count of the `CRegionObjectElement` object. |

### GetName

Gets the name of this auxiliary region.

```cpp
virtual const char* GetName() const = 0;
```

**Return value**

Returns a string representing the region name (e.g., "MRZ", "PortraitZone", "SignatureArea").

### GetConfidence

Gets the confidence level of this auxiliary region detection.

```cpp
virtual int GetConfidence() const = 0;
```

**Return value**

Returns the confidence value, typically in the range [0, 100].

### SetName

Sets the name of this auxiliary region.

```cpp
virtual void SetName(const char* name) = 0;
```

**Parameters**

`[in] name` The region name to set (e.g., "MRZ", "PortraitZone", "SignatureArea").

### SetLocation

Sets the location of this auxiliary region.

```cpp
virtual int SetLocation(const CQuadrilateral& location) = 0;
```

**Parameters**

`[in] location` A `CQuadrilateral` object defining the region boundaries.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**See Also**

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### SetConfidence

Sets the confidence level of this auxiliary region detection.

```cpp
virtual void SetConfidence(int confidence) = 0;
```

**Parameters**

`[in] confidence` The confidence value to set, typically in the range [0, 100].

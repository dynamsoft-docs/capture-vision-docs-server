---
layout: default-layout
title: class CPredetectedRegionElement - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, c++
needAutoGenerateSidebar: true
---

# CPredetectedRegionElement

The `CPredetectedRegionElement` class represents a region element that has been pre-detected in an image. It is a subclass of the `CRegionObjectElement`.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CPredetectedRegionElement

```cpp
class CPredetectedRegionElement : public CRegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetModeName`](#getmodename)   | Gets the name of the detection mode used to detect this region element. |
| [`SetLocation`](#setlocation)   | Sets the location of the region object element. |
| [`GetLabelId`](#getlabelid)     | Gets the label id of the region object element. |
| [`GetLabelName`](#getlabelname) | Gets the label name of the region object element. |
| **Methods Inherited from [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html):** | |
| [`GetLocation`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object element. |
| [`GetReferencedElement`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`GetElementType`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getelementtype) | Gets the type of the region object element. |
| [`GetImageData`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the image data for the element. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#clone) | Creates a copy of the region object element. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#retain) | Increases the reference count of the region object element. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html#release) | Decreases the reference count of the region object element. |

### GetModeName

Gets the name of the detection mode used to detect this region element.

```cpp
virtual const char* GetModeName() const;
```

**Return value**

Returns the name of the detection mode used to detect this region element.

### SetLocation

Set the location of the region object element.

```cpp
virtual int SetLocation(const CQuadrilateral& location) = 0;
```

**Parameters**

`location` The location of the region object element.

**Return value**

Returns 0 if success, otherwise an error code.

### GetLabelId

Gets the label id of the predetected region element.

```cpp
virtual int GetLabelId() const = 0;
```

**Return value**

Returns the label id of the predetected region element.

### GetLabelName

Gets the label name of the predetected region element.

```cpp
virtual const char* GetLabelName() const = 0;
```

**Return value**

Returns the label name of the predetected region element.
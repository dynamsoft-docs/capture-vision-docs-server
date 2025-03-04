---
layout: default-layout
title: class CScaledColourImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CScaledColourImageUnit in Dynamsoft Core Module.
keywords: scaled down colour image, c++
needAutoGenerateSidebar: true
---

# CScaledColourImageUnit

The `CScaledColourImageUnit` class represents an intermediate result unit that contains scaled color image. It is derived from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CScaledColourImageUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the unit.|
| [`SetImageData`](#setimagedata) | Sets the image data of the unit. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetImageData

Gets the image data of the unit.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the `CImageData` object that contains the image data of the unit. You are not required to release the memory pointed to by the returned pointer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetImageData

Sets the image data of the unit.

**Parameters**

imgData The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

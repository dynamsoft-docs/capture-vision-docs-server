---
layout: default-layout
title: class CBinaryImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, c++
needAutoGenerateSidebar: true
---

# CBinaryImageUnit

The `CBinaryImageUnit` class represents a unit that contains a binary image. It inherits from the `CIntermediateResultUnit` class and stores binary image data.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CBinaryImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the binary image data. |
| [`SetImageData`](#setimagedata) | Sets the binary image data. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetImageData

Gets the binary image data.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the `CBinaryImageData` object containing the binary image data. You don't need to release the memory pointed to by the returned pointer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetImageData

Sets the binary image data.

**Parameters**

imgData The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

---
layout: default-layout
title: class CGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CGrayscaleImageUnit in Dynamsoft Core Module.
keywords: grayscale image, c++
needAutoGenerateSidebar: true
---

# CGrayscaleImageUnit

The `CGrayscaleImageUnit` class represents a grayscale image unit. It is derived from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CGrayscaleImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the grayscale image. |
| [`SetImageData`](#setimagedata) | Sets the grayscale image. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetImageData

Gets the grayscale image.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a pointer to the `CImageData` object that contains the grayscale image. You are not required to release the memory pointed to by the returned pointer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetImageData

Sets the grayscale image.

**Parameters**

imgData The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

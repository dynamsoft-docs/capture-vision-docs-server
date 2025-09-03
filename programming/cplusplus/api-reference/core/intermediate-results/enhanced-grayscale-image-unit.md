---
layout: default-layout
title: class CEnhancedGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CEnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: enhanced grayscale image, c++
needAutoGenerateSidebar: true
---

# CEnhancedGrayscaleImageUnit

The `CEnhancedGrayscaleImageUnit` class represents an intermediate result unit that contains an enhanced grayscale image data. Gray enhancement methods include gray equalization, gray smoothing, gray sharpening and smoothing.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CEnhancedGrayscaleImageUnit  : public CIntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the enhanced grayscale image data. |
| [`SetImageData`](#setimagedata) | Sets the enhanced grayscale image data. |

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetImageData

Gets the enhanced grayscale image data.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a const pointer to the `CImageData` object that contains the enhanced grayscale image data. You don't need to release the memory pointed to by the returned pointer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetImageData

Sets the enhanced grayscale image data.

**Parameters**

imgData The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

```cpp
virtual int SetImageData(const CImageData* imgData) = 0;
```

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

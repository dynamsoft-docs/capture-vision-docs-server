---
layout: default-layout
title: class EnhancedGrayscaleImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class EnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: enhanced grayscale image, .NET
needAutoGenerateSidebar: true
---

# EnhancedGrayscaleImageUnit

The `EnhancedGrayscaleImageUnit` class represents an intermediate result unit that contains an enhanced grayscale image data. Gray enhancement methods include gray equalization, gray smoothing, gray sharpening and smoothing.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class EnhancedGrayscaleImageUnit  : IntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the enhanced grayscale image data. |
| [`SetImageData`](#setimagedata) | Sets the enhanced grayscale image data. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the enhanced grayscale image data.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object that contains the enhanced grayscale image data.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the enhanced grayscale image data.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

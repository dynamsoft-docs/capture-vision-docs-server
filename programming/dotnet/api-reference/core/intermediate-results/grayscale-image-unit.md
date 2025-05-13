---
layout: default-layout
title: class GrayscaleImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class GrayscaleImageUnit in Dynamsoft Core Module.
keywords: grayscale image, .NET
needAutoGenerateSidebar: true
---

# GrayscaleImageUnit

The `GrayscaleImageUnit` class represents a grayscale image unit. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class GrayscaleImageUnit : IntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the grayscale image. |
| [`SetImageData`](#setimagedata) | Sets the grayscale image. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the grayscale image.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object that contains the grayscale image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the grayscale image.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

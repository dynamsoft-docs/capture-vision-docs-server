---
layout: default-layout
title: class TransformedGrayscaleImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: transformed grayscale image, .NET
needAutoGenerateSidebar: true
---

# TransformedGrayscaleImageUnit

The `TransformedGrayscaleImageUnit` class is a subclass of `IntermediateResultUnit` that represents a transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TransformedGrayscaleImageUnit : IntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the transformed grayscale image.|
| [`SetImageData`](#setimagedata) | Sets the transformed grayscale image. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the image data of the transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

```csharp
ImageData GetImageData()
```

**Return value**

Returns an `ImageData` object that represents the image data of the transformed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the transformed grayscale image.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

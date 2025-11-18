---
layout: default-layout
title: class TextureRemovedGrayscaleImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: text removed grayscale image, .NET
needAutoGenerateSidebar: true
---

# TextureRemovedGrayscaleImageUnit

The `TextureRemovedGrayscaleImageUnit` class represents an intermediate result unit that contains texture-removed grayscale image data.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextureRemovedGrayscaleImageUnit : IntermediateResultUnit 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the texture-removed grayscale image. |
| [`SetImageData`](#setimagedata) | Sets the texture-removed grayscale image. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the texture-removed grayscale image.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the texture-removed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the texture-removed grayscale image.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

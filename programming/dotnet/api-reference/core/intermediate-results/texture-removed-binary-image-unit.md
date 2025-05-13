---
layout: default-layout
title: class TextureRemovedBinaryImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextureRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: texture removed binary image, .NET
needAutoGenerateSidebar: true
---

# TextureRemovedBinaryImageUnit

The `TextureRemovedBinaryImageUnit` class represents an intermediate result unit that stores texture-removed binary image data.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextureRemovedBinaryImageUnit : IntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the texture-removed binary image. |
| [`SetImageData`](#setimagedata) | Sets the texture-removed binary image. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the texture-removed binary image.

```csharp
ImageData GetImageData()
```

**Return value**

Returns an `ImageData` object that represents the texture-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the texture-removed binary image.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

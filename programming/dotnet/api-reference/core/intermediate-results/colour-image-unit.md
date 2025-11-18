---
layout: default-layout
title: class ColourImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ColourImageUnit in Dynamsoft Core Module.
keywords: colour image, .NET
needAutoGenerateSidebar: true
---

# ColourImageUnit

The `ColourImageUnit` class represents a unit that contains color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class ColourImageUnit : IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the color image unit. |
| [`SetImageData`](#setimagedata) | Sets the image data of the color image unit. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the image data of the color image unit.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object that contains the image data of the color image unit.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the image data of the color image unit.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

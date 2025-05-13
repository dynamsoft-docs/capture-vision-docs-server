---
layout: default-layout
title: class ScaledColourImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ScaledColourImageUnit in Dynamsoft Core Module.
keywords: scaled down colour image, .NET
needAutoGenerateSidebar: true
---

# ScaledColourImageUnit

The `ScaledColourImageUnit` class represents an intermediate result unit that contains scaled color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class ScaledColourImageUnit : IntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data of the unit.|
| [`SetImageData`](#setimagedata) | Sets the image data of the unit. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the image data of the unit.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object that contains the image data of the unit.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the image data of the unit.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

---
layout: default-layout
title: class BinaryImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class BinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, .NET
needAutoGenerateSidebar: true
---

# BinaryImageUnit

The `BinaryImageUnit` class represents a unit that contains a binary image. It inherits from the `IntermediateResultUnit` class and stores binary image data.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class BinaryImageUnit : IntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the binary image data. |
| [`SetImageData`](#setimagedata) | Sets the binary image data. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the binary image data.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object containing the binary image data.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the binary image data.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`[in] imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

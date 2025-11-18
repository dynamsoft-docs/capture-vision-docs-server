---
layout: default-layout
title: class TextRemovedBinaryImageUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: text removed binary image, .NET
needAutoGenerateSidebar: true
---

# TextRemovedBinaryImageUnit

The `TextRemovedBinaryImageUnit` class represents an intermediate result unit that contains a text-removed binary image.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextRemovedBinaryImageUnit : IntermediateResultUnit 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the text-removed binary image. |
| [`SetImageData`](#setimagedata) | Sets the text-removed binary image. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetImageData

Gets the text-removed binary image.

```csharp
ImageData GetImageData()
```

**Return value**

Returns the `ImageData` object that contains the text-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageData

Sets the text-removed binary image.

```csharp
int SetImageData(ImageData imgData)
```

**Parameters**

`imgData` The image data to set.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

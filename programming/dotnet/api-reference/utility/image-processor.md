---
layout: default-layout
title: class ImageProcessor - Dynamsoft Utility Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ImageProcessor in Dynamsoft Utility Module.
keywords: image processor, .NET
needAutoGenerateSidebar: true
---

# ImageProcessor

The `ImageProcessor` class is a utility class for applying advanced processing on images.

## Definition

*Namespace:* Dynamsoft.Utility


```csharp
class ImageProcessor : IDisposable
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`AdjustBrightness`](#adjustbrightness) | Adjusts the brightness of the image. |
| [`AdjustContrast`](#adjustcontrast) | Adjusts the contrast of the image. |
| [`ConvertToBinaryGlobal`](#converttobinaryglobal) | Converts the grayscale image to binary image using a global threshold. |
| [`ConvertToBinaryLocal`](#converttobinarylocal) | Converts the grayscale image to binary image using local (adaptive) binarization. |
| [`ConvertToGray`](#converttogray) | Converts colour image to grayscale. |
| [`CropImage`](#cropimage) | Crops an image. |
| [`CropAndDeskewImage`](#cropanddeskewimage) | Crops and deskews a region from the input image based on the specified quadrilateral. |
| [`FilterImage`](#filterimage) | Applies a specified image filter to an input image and returns the filtered result. |

### AdjustBrightness

Adjusts the brightness of the image.

```csharp
ImageData AdjustBrightness(ImageData imageData, int brightness)
```

**Parameters**

`[in] imageData` The image data to be processed.

`[in] brightness` Brightness adjustment value (positive values increase brightness, negative values decrease brightness). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### AdjustContrast

Adjusts the contrast of the image.

```csharp
ImageData AdjustContrast(ImageData imageData, int contrast)
```

**Parameters**

`[in] imageData` The image data to be processed.

`[in] contrast` Contrast adjustment value (positive values enhance, negative values reduce contrast). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### ConvertToBinaryGlobal

Converts an input image to a binary image using a global threshold. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```csharp
ImageData ConvertToBinaryGlobal(ImageData imageData, int threshold = -1, bool invert = false)
```

**Parameters**

`[in] imageData` Input image (grayscale, color, or binary).

`[in] threshold` Global threshold for binarization. If set to -1 (default), the function will automatically compute an optimal threshold.

`[in] invert` If true, invert the output binary image.

**Return value**

Returns an `ImageData` object representing the binarized image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### ConvertToBinaryLocal

Converts an input image to a binary image using local (adaptive) thresholding. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```csharp
ImageData ConvertToBinaryLocal(ImageData imageData, int blockSize = 0, int compensation = 10, bool invert = false)
```

**Parameters**

`[in] imageData` Input image (grayscale, color, or binary).

`[in] blockSize` Size of the local block used for adaptive thresholding. If set to 0 (default), a suitable block size will be chosen automatically.

`[in] compensation` Adjustment value applied to the computed local threshold (default 10).

`[in] invert` If true, invert the output binary image.

**Return value**

Returns an `ImageData` object representing the locally binarized image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

**Remarks**

Changed default value of `compensation` parameter from 0 to 10 in Dynamsoft Barcode Reader SDK version 11.4.1000 and Dynamsoft Capture Vision version 3.4.1000.

### ConvertToGray

Converts colour image to grayscale.

```csharp
ImageData ConvertToGray(ImageData imageData, float R = 0.3f, float G = 0.59f, float B = 0.11f)
```

**Parameters**

`[in] imageData` The image data to be processed.

`[in] R` Weight for red channel.

`[in] G` Weight for green channel.

`[in] B` Weight for blue channel.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### CropImage

Crops an image.

```csharp
ImageData CropImage(ImageData imageData, Rect rect, out int errorCode);

//Announced as deprecated. Use CropAndDeskewImage instead.
ImageData CropImage(ImageData imageData, Quadrilateral quad, out int errorCode);
```

**Parameters**

`[in] imageData` The image data to be cropped.

`[in] rect` The rectangle to be cropped.

`[in] quad` The quadrilateral to be cropped.

`[out] errorCode` The error code.

**Return value**

Returns an `ImageData` object representing the cropped image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[Rect]({{ site.dcvb_dotnet_api }}core/basic-classes/rect.html)

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### CropAndDeskewImage

Crops and deskews a region from the input image based on the specified quadrilateral.

```cpp
ImageData CropAndDeskewImage(ImageData imageData, Quadrilateral quad, int dstWidth = 0, int dstHeight = 0, int padding = 0)
ImageData CropAndDeskewImage(ImageData imageData, Quadrilateral quad, int dstWidth, int dstHeight, int padding, out int errorCode)
```

**Parameters**

`[in] imageData` The source image to be cropped and deskewed.

`[in] quad` A quadrilateral defining the region of interest to extract.

`[in] dstWidth` (Optional) The width of the output image. If set to 0, the width and height will be automatically calculated.

`[in] dstHeight` (Optional) The height of the output image. If set to 0, the width and height will be automatically calculated.

`[in] padding` (Optional) Extra padding (in pixels) applied to expand the boundaries of the extracted region. Default is 0.

`[out] errorCode` The error code.

**Return value**

Returns an `ImageData` object representing the cropped image.

**Remarks**

The function will automatically calculate the perspective transform matrix and use it to crop the image.  
If the specified quadrilateral exceeds the image boundaries, white will be used to fill the exceeding area.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### FilterImage

Applies a specified image filter to an input image and returns the filtered result.

```csharp
ImageData FilterImage(ImageData imageData, EnumFilterType filterType)
```

**Parameters**

`[in] imageData` The image data to be processed.

`[in] filterType` Specifies the type of filter to apply to the input image.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[EnumFilterType]({{ site.dcvb_dotnet_api }}utility/enum-filter-type.html)


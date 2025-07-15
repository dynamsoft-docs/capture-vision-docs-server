---
layout: default-layout
title: class CImageProcessor - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageProcessor in Dynamsoft Utility Module.
keywords: image processor, c++
needAutoGenerateSidebar: true
---

# CImageProcessor

The `CImageProcessor` class is a utility class for applying advanced processing on images.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CImageProcessor
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

```cpp
CImageData* AdjustBrightness(const CImageData* pImageData, int brightness)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] brightness` Brightness adjustment value (positive values increase brightness, negative values decrease brightness). The value range is [-100, 100]

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### AdjustContrast

Adjusts the contrast of the image.

```cpp
CImageData* AdjustContrast(const CImageData* pImageData, int contrast)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] contrast` Contrast adjustment value (positive values enhance, negative values reduce contrast). The value range is [-100, 100]

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### ConvertToBinaryGlobal

Converts the grayscale image to binary image using a global threshold.

```cpp
CImageData* ConvertToBinaryGlobal(const CImageData* pImageData, int threshold = -1, bool invert = false)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] threshold` Global threshold for binarization(default is -1, automatic calculate the threshold).

`[in] invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### ConvertToBinaryLocal

Converts the grayscale image to binary image using local (adaptive) binarization.

```cpp
CImageData* ConvertToBinaryLocal(const CImageData* pImageData, int blockSize = 0, int compensation = 0, bool invert = false)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] blockSize` Size of the block for local binarization(default is 0).

`[in] compensation` Adjustment value to modify the threshold (default is 0).

`[in] invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### ConvertToGray

Converts colour image to grayscale.

```cpp
CImageData* ConvertToGray(const CImageData* pImageData, float R = 0.3f, float G = 0.59f, float B = 0.11f)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] R` Weight for red channel.

`[in] G` Weight for green channel.

`[in] B` Weight for blue channel.

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### CropImage

Crops an image.

```cpp
CImageData* CropImage(const CImageData* pImageData, const CRect& rect, int* pErrorCode = NULL)

//Announced as deprecated. Use CropAndDeskewImage instead.
CImageData* CropImage(const CImageData* pImageData, const CQuadrilateral& quad, int* pErrorCode = NULL)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be cropped.

`[in] rect` The rectangle to be cropped.

`[in] quad` The quadrilateral to be cropped.

`[out] pErrorCode` The error code.

**Return value**

Returns a pointer to a `CImageData` object representing the cropped image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

[CRect]({{ site.dcvb_cpp_api }}core/basic-structures/rect.html)

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### CropAndDeskewImage

Crops and deskews a region from the input image based on the specified quadrilateral.

```cpp
CImageData* CropAndDeskewImage(const CImageData* imageData, const CQuadrilateral& quad, int dstWidth = 0, int dstHeight = 0, int padding = 0, int* errorCode = NULL);
```

**Parameters**

`[in] imageData` A pointer to the source image to be cropped and deskewed.

`[in] quad` A quadrilateral defining the region of interest to extract.

`[in] dstWidth` (Optional) The width of the output image. If set to 0, the width and height will be automatically calculated.

`[in] dstHeight` (Optional) The height of the output image. If set to 0, the width and height will be automatically calculated.

`[in] padding` (Optional) Extra padding (in pixels) applied to expand the boundaries of the extracted region. Default is 0.

`[out] errorCode` The error code.

**Return value**

Returns a pointer to a `CImageData` object representing the cropped image.

**Remarks**

The caller is responsible for freeing the memory allocated for the cropped image.  
The function will automatically calculate the perspective transform matrix and use it to crop the image.  
If the specified quadrilateral exceeds the image boundaries, white will be used to fill the exceeding area.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### FilterImage

Applies a specified image filter to an input image and returns the filtered result.

```cpp
CImageData* FilterImage(const CImageData* pImageData, FilterType filterType)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be processed.

`[in] filterType` Specifies the type of filter to apply to the input image.

**Return value**

Returns a pointer to a `CImageData` object representing the processed image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

[FilterType]({{ site.dcvb_cpp_api }}utility/enum-filter-type.html)


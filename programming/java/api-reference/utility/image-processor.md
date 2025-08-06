---
layout: default-layout
title: class ImageProcessor - Dynamsoft Utility Module Java Edition API Reference
description: This page shows the Java Edition of the class ImageProcessor in Dynamsoft Utility Module.
keywords: image processor, java
needAutoGenerateSidebar: true
---

# ImageProcessor

The `ImageProcessor` class is a utility class for applying advanced processing on images.

## Definition

*Namespace:* com.dynamsoft.utility

```java
public class ImageProcessor
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageProcessor`](#imageprocessor) | Initializes a new instance of the `ImageProcessor` class. |
| [`adjustBrightness`](#adjustbrightness) | Adjusts the brightness of the image. |
| [`adjustContrast`](#adjustcontrast) | Adjusts the contrast of the image. |
| [`convertToBinaryGlobal`](#converttobinaryglobal) | Converts the grayscale image to binary image using a global threshold. |
| [`convertToBinaryLocal`](#converttobinarylocal) | Converts the grayscale image to binary image using local (adaptive) binarization. |
| [`convertToGray`](#converttogray) | Converts colour image to grayscale. |
| [`cropImage`](#cropimage) | Crops an image. |
| [`cropAndDeskewImage`](#cropanddeskewimage) | Crops and deskews a region from the input image based on the specified quadrilateral. |
| [`filterImage`](#filterimage) | Applies a specified image filter to an input image and returns the filtered result. |

### ImageProcessor

Initializes a new instance of the `ImageProcessor` class.

```java
ImageProcessor()
```

### adjustBrightness

Adjusts the brightness of the image.

```java
ImageData adjustBrightness(ImageData imageData, int brightness)
```

**Parameters**

`imageData` The image data to be processed.

`brightness` Brightness adjustment value (positive values increase brightness, negative values decrease brightness). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### adjustContrast

Adjusts the contrast of the image.

```java
ImageData adjustContrast(ImageData imageData, int contrast)
```

**Parameters**

`imageData` The image data to be processed.

`contrast` Contrast adjustment value (positive values enhance, negative values reduce contrast). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### convertToBinaryGlobal

Converts the grayscale image to binary image using a global threshold.

```java
ImageData convertToBinaryGlobal(ImageData imageData)
ImageData convertToBinaryGlobal(ImageData imageData, int threshold, boolean invert)
```

**Parameters**

`imageData` The image data to be processed.

`threshold` Global threshold for binarization(default is 0, automatic calculate the threshold).

`invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### convertToBinaryLocal

Converts the grayscale image to binary image using local (adaptive) binarization.

```java
ImageData convertToBinaryLocal(ImageData imageData)
ImageData convertToBinaryLocal(ImageData imageData, int blockSize, int compensation, boolean invert)
```

**Parameters**

`imageData` The image data to be processed.

`blockSize` Size of the block for local binarization(default is 0).

`compensation` Adjustment value to modify the threshold (default is 0).

`invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### convertToGray

Converts colour image to grayscale.

```java
ImageData convertToGray(ImageData imageData)
ImageData convertToGray(ImageData imageData, float R, float G, float B)
```

**Parameters**

`imageData` The image data to be processed.

`R` Weight for red channel.

`G` Weight for green channel.

`B` Weight for blue channel.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### cropImage

Crops an image.

```java
ImageData cropImage(ImageData imageData, Rect rect) throws UtilityException
@Deprecated
ImageData cropImage(ImageData imageData, Quadrilateral quad) throws UtilityException
```

**Parameters**

`imageData` The image data to be cropped.

`rect` The rectangular region to crop.

`quad` The quadrilateral region to crop.

**Return value**

Returns an `ImageData` object representing the processed image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[Rect]({{ site.dcvb_java_api }}core/basic-classes/rect.html)

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

**Remarks**

`cropImage` with `Quadrilateral` is announced as deprecated since version 3.0.4000. Use `cropAndDeskewImage` instead.

### cropAndDeskewImage

Crops and deskews a region from the input image based on the specified quadrilateral.

```java
ImageData cropAndDeskewImage(ImageData imageData, Quadrilateral quad) throws UtilityException
ImageData cropAndDeskewImage(ImageData imageData, Quadrilateral quad, int dstWidth, int dstHeight, int padding) throws UtilityException
```

**Parameters**

`imageData` The image data to be processed.

`quad` The quadrilateral shape to crop and deskew.

`dstWidth` The desired width of the output image.

`dstHeight` The desired height of the output image.

`padding` The padding around the cropped area.

**Return value**

Returns an `ImageData` object representing the processed image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### filterImage

Applies a specified image filter to an input image and returns the filtered result.

```java
ImageData filterImage(ImageData imageData, @EnumFilterType int filterType)
```

**Parameters**

`imageData` The image data to be processed.

`filterType` The type of filter to apply.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[EnumFilterType]({{ site.dcvb_java_api }}utility/enum-filter-type.html)
def crop_and_deskew_image(self, image_data: ImageData, crop_form: Quadrilateral, destination_width: int = 0, destination_height: int = 0, padding: int = 0) -> Tuple[int, ImageData]:
```

**Parameters**

`[in] image_data` The source image to be cropped and deskewed.

`[in] crop_form` A quadrilateral defining the region of interest to extract.

`[in] destination_width` (Optional) The width of the output image. If set to 0, the width and height will be automatically calculated.

`[in] destination_height` (Optional) The height of the output image. If set to 0, the width and height will be automatically calculated.

`[in] padding` (Optional) Extra padding (in pixels) applied to expand the boundaries of the extracted region. Default is 0.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `image_data` <*ImageData*>: An `ImageData` object representing the processed image.

**Remarks**

The function will automatically calculate the perspective transform matrix and use it to crop the image.  
If the specified quadrilateral exceeds the image boundaries, white will be used to fill the exceeding area.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### filter_image

Applies a specified image filter to an input image and returns the filtered result.

```java
def filter_image(self, image_data: ImageData, filter_type: FilterType) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`filter_type` Specifies the type of filter to apply to the input image.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[FilterType]({{ site.dcvb_cpp_api }}utility/enum-filter-type.html)


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

*Package:* com.dynamsoft.utility

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

Converts an input image to a binary image using a global threshold. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```java
ImageData convertToBinaryGlobal(ImageData imageData)
ImageData convertToBinaryGlobal(ImageData imageData, int threshold, boolean invert)
```

**Parameters**

`imageData` Input image (grayscale, color, or binary).

`threshold` Global threshold for binarization. If set to -1 (default), the function will automatically compute an optimal threshold.

`invert` If true, invert the output binary image.

**Return value**

Returns an `ImageData` object representing the binarized image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### convertToBinaryLocal

Converts an input image to a binary image using local (adaptive) thresholding. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```java
ImageData convertToBinaryLocal(ImageData imageData)
ImageData convertToBinaryLocal(ImageData imageData, int blockSize, int compensation, boolean invert)
```

**Parameters**

`imageData` Input image (grayscale, color, or binary).

`blockSize` Size of the local block used for adaptive thresholding. If set to 0 (default), a suitable block size will be chosen automatically.

`compensation` Adjustment value applied to the computed local threshold (default 10).

`invert` If true, invert the output binary image (default false).

**Return value**

Returns an `ImageData` object representing the locally binarized image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

**Remarks**

Changed default value of `compensation` parameter from 0 to 10 in Dynamsoft Barcode Reader SDK version 11.4.1000 and Dynamsoft Capture Vision version 3.4.1000.

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

**Remarks**

The function will automatically calculate the perspective transform matrix and use it to crop the image.  
If the specified quadrilateral exceeds the image boundaries, white will be used to fill the exceeding area.

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


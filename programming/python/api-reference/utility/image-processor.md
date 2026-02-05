---
layout: default-layout
title: class ImageProcessor - Dynamsoft Utility Module Python Edition API Reference
description: This page shows the Python Edition of the class ImageProcessor in Dynamsoft Utility Module.
keywords: image processor, python
needAutoGenerateSidebar: true
---

# ImageProcessor

The `ImageProcessor` class is a utility class for applying advanced processing on images.

## Definition

*Module:* utility

```python
class ImageProcessor:
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`adjust_brightness`](#adjust_brightness) | Adjusts the brightness of the image. |
| [`adjust_contrast`](#adjust_contrast) | Adjusts the contrast of the image. |
| [`convert_to_binary_global`](#convert_to_binary_global) | Converts the grayscale image to binary image using a global threshold. |
| [`convert_to_binary_local`](#convert_to_binary_local) | Converts the grayscale image to binary image using local (adaptive) binarization. |
| [`convert_to_gray`](#convert_to_gray) | Converts colour image to grayscale. |
| [`crop_image`](#crop_image) | Crops an image. |
| [`crop_and_deskew_image`](#crop_and_deskew_image) | Crops and deskews a region from the input image based on the specified quadrilateral. |
| [`filter_image`](#filter_image) | Applies a specified image filter to an input image and returns the filtered result. |

### adjust_brightness

Adjusts the brightness of the image.

```python
def adjust_brightness(self, image_data: ImageData, brightness: int) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`brightness` Brightness adjustment value (positive values increase brightness, negative values decrease brightness). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### adjust_contrast

Adjusts the contrast of the image.

```python
def adjust_contrast(self, image_data: ImageData, contrast: int) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`contrast` Contrast adjustment value (positive values enhance, negative values reduce contrast). The value range is [-100, 100]

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### convert_to_binary_global

Converts an input image to a binary image using a global threshold. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```python
def convert_to_binary_global(self, image_data: ImageData, threshold: int = -1, invert: bool = False) -> ImageData:
```

**Parameters**

`image_data` Input image (grayscale, color, or binary).

`threshold` Global threshold for binarization. If set to -1 (default), the function will automatically compute an optimal threshold.

`invert` If true, invert the output binary image.

**Return value**

Returns an `ImageData` object representing the binarized image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### convert_to_binary_local

Converts an input image to a binary image using local (adaptive) thresholding. Supports grayscale, color, and binary input images (color images are internally converted to grayscale before thresholding).

```python
def convert_to_binary_local(self, image_data: ImageData, block_size: int = 0, compensation: int = 10, invert: bool = False) ->ImageData:
```

**Parameters**

`image_data` Input image (grayscale, color, or binary).

`block_size` Size of the local block used for adaptive thresholding. If set to 0 (default), a suitable block size will be chosen automatically.

`compensation` Adjustment value applied to the computed local threshold (default 10).

`invert` If true, invert the output binary image (default False).

**Return value**

Returns an `ImageData` object representing the locally binarized image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

**Remarks**

Changed default value of `compensation` parameter from 0 to 10 in Dynamsoft Barcode Reader SDK version 11.4.1000 and Dynamsoft Capture Vision version 3.4.1000.

### convert_to_gray

Converts colour image to grayscale.

```python
def convert_to_gray(self, image_data: ImageData, r: float = 0.3, g: float = 0.59, b: float = 0.11) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`r` Weight for red channel.

`g` Weight for green channel.

`b` Weight for blue channel.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### crop_image

Crops an image.

```python
def crop_image(self, image_data:ImageData, crop_form: Union[Rect,Quadrilateral]) -> Tuple[int, ImageData]:
```

**Parameters**

`image_data` The image data to be cropped.

`crop_form` The cropping form.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `image_data` <*ImageData*>: An `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[Rect]({{ site.dcvb_python_api }}core/basic-classes/rect.html)

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

**Remarks**

`crop_image` with `Quadrilateral` is announced as deprecated since version 3.0.4000. Use `crop_and_deskew_image` instead.

### crop_and_deskew_image

Crops and deskews a region from the input image based on the specified quadrilateral.

```cpp
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

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### filter_image

Applies a specified image filter to an input image and returns the filtered result.

```python
def filter_image(self, image_data: ImageData, filter_type: FilterType) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`filter_type` Specifies the type of filter to apply to the input image.

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[FilterType]({{ site.dcvb_cpp_api }}utility/enum-filter-type.html)


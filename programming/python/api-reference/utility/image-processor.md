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

*Module:* dynamsoft_utility

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

Converts the grayscale image to binary image using a global threshold.

```python
def convert_to_binary_global(self, image_data: ImageData, threshold: int = -1, invert: bool = False) -> ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`threshold` Global threshold for binarization(default is -1, automatic calculate the threshold).

`invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### convert_to_binary_local

Converts the grayscale image to binary image using local (adaptive) binarization.

```python
def convert_to_binary_local(self, image_data: ImageData, block_size: int = 0, compensation: int = 0, invert: bool = False) ->ImageData:
```

**Parameters**

`image_data` The image data to be processed.

`block_size` Size of the block for local binarization(default is 0).

`compensation` Adjustment value to modify the threshold (default is 0).

`invert` If true, invert the binary image (black becomes white and white becomes black).

**Return value**

Returns an `ImageData` object representing the processed image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

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

`crop_form` The cropping form

**Return value**

Returns an `ImageData` object representing the cropped image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[Rect]({{ site.dcvb_python_api }}core/basic-classes/rect.html)

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


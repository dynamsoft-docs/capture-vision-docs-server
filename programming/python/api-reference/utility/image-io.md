---
layout: default-layout
title: class ImageIO - Dynamsoft Utility Module Python Edition API Reference
description: This page shows the Python Edition of the class ImageIO in Dynamsoft Utility Module.
keywords: image io, python
needAutoGenerateSidebar: true
---

# ImageIO

The `ImageIO` class handles image reading and writing (from/to files and memory).

## Definition

*Module:* dynamsoft_utility

```python
class ImageIO:
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`read_from_file`](#read_from_file) | Reads an image from a file. |
| [`read_from_memory`](#read_from_memory) | Reads an image from a file in memory. |
| [`read_from_numpy`](#read_from_numpy) | Reads an image from a numpy array. |
| [`save_to_file`](#save_to_file) | Saves an image to a file. |
| [`save_to_memory`](#save_to_memory) | Saves an image to a file in memory. |
| [`save_to_numpy`](#save_to_numpy) | Saves an image to a numpy array. |

### read_from_file

Reads an image from a file.

```python
def read_from_file(self, file_path: str) -> Tuple[int, ImageData]:
```

**Parameters**

`file_path` The path of the image file.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `image_data` <*ImageData*>: An `ImageData` object representing the image.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file. The caller is responsible for freeing the memory allocated for the image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### read_from_memory

Reads an image from a file in memory.

```python
def read_from_memory(self, image_file_bytes: bytes) -> Tuple[int, ImageData]:
```

**Parameters**

`image_file_bytes` A bytes representing the image file in memory.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `image_data` <*ImageData*>: An `ImageData` object representing the image.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file. The caller is responsible for freeing the memory allocated for the image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### read_from_numpy

Reads an image from a numpy array.

```python
def read_from_numpy(self, image: "numpy.ndarray", image_pixel_format: EnumImagePixelFormat) -> Tuple[int, str, ImageData]:
```

**Parameters**

`image` A numpy array representing the image.

`image_pixel_format` The pixel format of the image.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `image_data` <*ImageData*>: An `ImageData` object representing the image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[EnumImagePixelFormat]({{ site.dcvb_python_api }}core/enum-image-pixel-format.html)

### save_to_file

Saves an image to a file.

```python
def save_to_file(self, image_data: ImageData, path: str, overwrite: bool = True) -> Tuple[int, str]:
```

**Parameters**

`image_data` The image data to be saved.

`path` The targeting file path with the file name and extension name.

`overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### save_to_memory

Saves an image to a file in memory.

```python
def save_to_memory(self, image_data: ImageData,image_format: EnumImageFileFormat) -> Tuple[int, bytes]:
```

**Parameters**

`image_data` The image data to be saved.

`image_format` The image file format to be saved.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `image_file_bytes` <*bytes*>: The byte array representing the saved image file.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[EnumImageFileFormat]({{ site.dcvb_python_api }}core/enum-image-file-format.html)

### save_to_numpy

Saves an image to a numpy array.

```python
def save_to_numpy(self, image_data: ImageData) -> Tuple[int, str, "numpy.ndarray"]:
```

**Parameters**

`image_data` The image data to be saved.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `image` <*np.ndarray*>: A numpy array representing the saved image.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[EnumImageFileFormat]({{ site.dcvb_python_api }}core/enum-image-file-format.html)

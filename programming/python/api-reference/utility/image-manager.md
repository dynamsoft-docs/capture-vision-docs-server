---
layout: default-layout
title: ImageManager Class - Dynamsoft Utility Module Python Edition API Reference
description: Definition of ImageManager class in Dynamsoft Utility Module Python Edition.
keywords: image manager, drawing on image, python
needAutoGenerateSidebar: true
---

# ImageManager

The `ImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Module:* dynamsoft_utility

```python
class ImageManager
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `ImageManager` class. |
| [`save_to_file`](#save_to_file) | Saves an image to a file. |

### \_\_init\_\_

Initializes a new instance of the `ImageManager` class.

```python
def __init__(self):
```

### save_to_file

Saves an image to a file.

```python
def save_to_file(self, image_data: ImageData, path: str, overwrite: bool = True) -> Tuple[int, str]:
```

**Parameters**

`image_data` The image data to be saved.

`path` The targeting file path with the file name and extension name.

`overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)


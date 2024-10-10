---
layout: default-layout
title: FileFetcher Class - Dynamsoft Utility Module Python Edition API Reference
description: Definition of FileFetcher class in Dynamsoft Utility Module Python Edition.
keywords: file fetcher, python
needAutoGenerateSidebar: true
---

# FileFetcher

The `FileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `ImageSourceAdapter` class.

## Definition

*Module:* dynamsoft_utility

*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_python_api }}core/basic-classes/image-source-adapter.html) -> FileFetcher

```python
class FileFetcher(dynamsoft_core.ImageSourceAdapter)
```

## Methods

| Method | Description |
|--------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `FileFetcher` class. |
| [`set_file`](#set_file) | Sets the file using a file path, file bytes or an `ImageData` object. |
| [`set_pdf_reading_parameter`](#set_pdf_reading_parameter) | Sets the parameters for reading PDF files. |
| [`set_pages`](#set_pages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| [`has_next_image_to_fetch`](#has_next_image_to_fetch) | Determines whether there are more images left to fetch. |

### \_\_init\_\_

Initializes a new instance of the `FileFetcher` class.

```python
def __init__(self):
```

### set_file

Sets the file using a file path, file bytes or an `ImageData` object.

```python
def set_file(self, *args) -> Tuple[int, str]:
```

**Parameters**

`args` <*tuple*>: A variable-length argument list. Can be one of the following:

- `file_path` <*str*>: Specifies the path of the file to process.
- `file_bytes` <*bytes*>: Specifies the image file bytes in memory to process.
- `image_data` <*ImageData*>: Specifies the image data to process.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_pdf_reading_parameter

Sets the parameters for reading PDF files.

```python
def set_pdf_reading_parameter(self, para: PDFReadingParameter) -> Tuple[int, str]:
```

**Parameters**

`para` A `PDFReadingParameter` object with PDF files reading parameters.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[PDFReadingParameter]({{ site.dcvb_python_api }}core/basic-classes/pdf-reading-parameter.html)

### set_pages

Sets the 0-based page indexes of a file (.tiff or .pdf). By default, there is no restriction on the number of pages that can be processed in a single file.

```python
def set_pages(self, pages: List[int]) -> Tuple[int, str]:
```

**Parameters**

`pages` An integer list containing the page information to be set.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

### has_next_image_to_fetch

Determines whether there are more images left to fetch.

```python
def has_next_image_to_fetch(self) -> bool:
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

---
layout: default-layout
title: DirectoryFetcher Class - Dynamsoft Utility Module Python Edition API Reference
description: Definition of DirectoryFetcher class in Dynamsoft Utility Module Python Edition.
keywords: directory fetcher, python
needAutoGenerateSidebar: true
---

# DirectoryFetcher

The `DirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `ProactiveImageSourceAdapter` class.

## Definition

*Module:* dynamsoft_utility

*Inheritance:* [ProactiveImageSourceAdapter]({{ site.dcvb_python_api }}utility/proactive-image-source-adapter.html) -> DirectoryFetcher

```python
class DirectoryFetcher(ProactiveImageSourceAdapter)
```

## Methods

| Method | Description |
|--------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `DirectoryFetcher` class. |
| [`set_directory`](#set_directory) | Sets the directory path and filter for the file search. |
| [`set_pdf_reading_parameter`](#set_pdf_reading_parameter) | Sets the parameters for reading PDF files. |
| [`set_pages`](#set_pages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| [`has_next_image_to_fetch`](#has_next_image_to_fetch) | Determines whether there are more images left to fetch. |

### \_\_init\_\_

Initializes a new instance of the `DirectoryFetcher` class.

```python
def __init__(self):
```

### set_directory

Sets the directory path and filter for the file search.

```python
def set_directory(self, *args) -> Tuple[int, str]:
```

**Parameters**

`args` <*tuple*>: A variable-length argument list that must contain following parameters in order:

- `path` <*str*>: The path of the directory to search.
- `filter` <*str*, optional>: A string that specifies file extensions. For example: "\*.BMP;\*.JPG;\*.GIF", or "\*.\*", etc. The default value is "\*.bmp;\*.jpg;\*.jpeg;\*.tif;\*.png;\*.tiff;\*.gif;\*.pdf".
- `recursive` <*bool*, optional>: Specifies whether to load files recursively. The default value is False.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

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


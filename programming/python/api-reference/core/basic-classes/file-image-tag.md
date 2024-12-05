---
layout: default-layout
title: FileImageTag Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of FileImageTag class in Dynamsoft Core Module Python Edition.
keywords: file image tag, python
needAutoGenerateSidebar: true
---

# FileImageTag

The `FileImageTag` class represents an image tag that is associated with a file. It inherits from the `ImageTag` class and adds additional attributes.

## Definition

*Module:* dynamsoft_core

```python
class FileImageTag(ImageTag)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `FileImageTag` class. |
| [`get_file_path`](#get_file_path) | Gets the file path of the image. |
| [`get_page_number`](#get_page_number) | Gets the page number of the current image in the Multi-Page image file. |
| [`get_total_pages`](#get_total_pages) | Gets the total page number of the Multi-Page image file. |
| [`get_type`](#get_type) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |

### \_\_init\_\_

Initializes a new instance of the `FileImageTag` class.

```python
def __init__(self, file_path: str, page_number: int, total_pages: int):
```

**Parameters**

`file_path` The file path of the image tag.

`page_number` The page number of the current image in the Multi-Page image file.

`total_pages` The total page number of the Multi-Page image file.

### get_file_path

Gets the file path of the image.

```python
def get_file_path(self) -> str:
```

**Return Value**

Returns the file path of the image tag.

### get_page_number

Gets the page number of the current image in the Multi-Page image file.

```python
def get_page_number(self) -> int:
```

**Return Value**

Returns the page number of the current image in the Multi-Page image file.

### get_total_pages

Gets the total page number of the Multi-Page image file.

```python
def get_total_pages(self) -> int:
```

**Return Value**

Returns the total page number of the Multi-Page image file.

### get_type

Gets the type of the image tag.

```python
def get_type(self) -> int:
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_enumerations }}core/image-tag-type.html?lang=python)

### clone

Creates a copy of the image tag.

```python
def clone(self) -> "FileImageTag":
```

**Return Value**

Returns a copy of the `FileImageTag` object.

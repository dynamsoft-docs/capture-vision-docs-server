---
layout: default-layout
title: OriginalImageResultItem Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of OriginalImageResultItem class in Dynamsoft Core Module Python Edition.
keywords: original image, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` class represents a captured original image result item. It is a derived class of `CapturedResultItem` and provides an class to get the image data.

## Definition

*Module:* dynamsoft_core

```python
class OriginalImageResultItem(CapturedResultItem)
```

## Methods

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`get_image_data`](#get_image_data) | Gets the image data for the `OriginalImageResultItem`. |

### get_image_data

Gets the image data for the `OriginalImageResultItem`.

```python
def get_image_data(self) -> "ImageData":
```

**Return Value**

Returns the `ImageData` object that contains the image data for the `OriginalImageResultItem`.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)


---
layout: default-layout
title: OriginalImageResultItem Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of OriginalImageResultItem class in Dynamsoft Core Module Java Edition.
keywords: original image, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` class represents a captured original image result item. It is a derived class of `CapturedResultItem` and provides an class to get the image data.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class OriginalImageResultItem extends CapturedResultItem
```

## Methods

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`getImageData`](#getimagedata) | Gets the image data for the `OriginalImageResultItem`. |

### getImageData

Gets the image data for the `OriginalImageResultItem`.

```java
ImageData getImageData()
```

**Return Value**

Returns the `ImageData` object that contains the image data for the `OriginalImageResultItem`.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)


---
layout: default-layout
title: class TransformedGrayscaleImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TransformedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: transformed grayscale image, java
needAutoGenerateSidebar: true
---

# TransformedGrayscaleImageUnit

The `TransformedGrayscaleImageUnit` class is a subclass of `IntermediateResultUnit` that represents a transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

```java
public class TransformedGrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the transformed grayscale image.|
| [`setImageData`](#setimagedata) | Sets the transformed grayscale image. |

### getImageData

Gets the image data of the transformed grayscale image. It may be the original grayscale image or the inverted image of the original grayscale image.

```java
ImageData getImageData()
```

**Return value**

Returns a `ImageData` object that represents the image data of the transformed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the transformed grayscale image.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

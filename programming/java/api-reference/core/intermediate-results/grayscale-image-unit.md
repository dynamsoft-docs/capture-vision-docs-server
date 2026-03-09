---
layout: default-layout
title: class GrayscaleImageUnit - Dynamsoft Core Module Java Edition API Reference
description: API reference for the GrayscaleImageUnit class in Dynamsoft Core Module Java Edition, which represents an intermediate result unit containing a grayscale image.
keywords: grayscale image, java
needAutoGenerateSidebar: true
---

# GrayscaleImageUnit

The `GrayscaleImageUnit` class represents a grayscale image unit. It is derived from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class GrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the grayscale image. |
| [`setImageData`](#setimagedata) | Sets the grayscale image. |

### getImageData

Gets the grayscale image.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the grayscale image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the grayscale image.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)


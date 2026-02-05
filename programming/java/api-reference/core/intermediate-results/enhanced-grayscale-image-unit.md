---
layout: default-layout
title: class EnhancedGrayscaleImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class EnhancedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: enhanced grayscale image, java
needAutoGenerateSidebar: true
---

# EnhancedGrayscaleImageUnit

The `EnhancedGrayscaleImageUnit` class represents an intermediate result unit that contains an enhanced grayscale image data. Gray enhancement methods include gray equalization, gray smoothing, gray sharpening and smoothing.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class EnhancedGrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the enhanced grayscale image data. |
| [`setImageData`](#setimagedata) | Sets the enhanced grayscale image data. |

### getImageData

Gets the enhanced grayscale image data.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the enhanced grayscale image data.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the enhanced grayscale image data.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

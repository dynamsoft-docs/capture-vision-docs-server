---
layout: default-layout
title: class TextureRemovedGrayscaleImageUnit - Dynamsoft Core Module Java Edition API Reference
description: API reference for the TextureRemovedGrayscaleImageUnit class in Dynamsoft Core Module Java Edition, which represents an intermediate result unit containing a grayscale image with texture removed.
keywords: text removed grayscale image, java
needAutoGenerateSidebar: true
---

# TextureRemovedGrayscaleImageUnit

The `TextureRemovedGrayscaleImageUnit` class represents an intermediate result unit that contains texture-removed grayscale image data.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextureRemovedGrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the texture-removed grayscale image. |
| [`setImageData`](#setimagedata) | Sets the texture-removed grayscale image. |

### getImageData

Gets the texture-removed grayscale image.

```java
ImageData getImageData()
```

**Return value**

Returns a texture-removed grayscale image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the texture-removed grayscale image.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

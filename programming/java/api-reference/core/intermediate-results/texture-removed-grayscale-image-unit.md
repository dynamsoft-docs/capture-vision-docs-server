---
layout: default-layout
title: class TextureRemovedGrayscaleImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: text removed grayscale image, java
needAutoGenerateSidebar: true
---

# TextureRemovedGrayscaleImageUnit

The `TextureRemovedGrayscaleImageUnit` class represents an intermediate result unit that contains texture-removed grayscale image data.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

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

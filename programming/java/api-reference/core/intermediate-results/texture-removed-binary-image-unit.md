---
layout: default-layout
title: class TextureRemovedBinaryImageUnit - Dynamsoft Core Module Java Edition API Reference
description: API reference for the TextureRemovedBinaryImageUnit class in Dynamsoft Core Module Java Edition, which represents an intermediate result unit containing a binary image with texture removed.
keywords: texture removed binary image, java
needAutoGenerateSidebar: true
---

# TextureRemovedBinaryImageUnit

The `TextureRemovedBinaryImageUnit` class represents an intermediate result unit that stores texture-removed binary image data.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextureRemovedBinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the texture-removed binary image. |
| [`setImageData`](#setimagedata) | Sets the texture-removed binary image. |

### getImageData

Gets the texture-removed binary image.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that represents the texture-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the texture-removed binary image.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

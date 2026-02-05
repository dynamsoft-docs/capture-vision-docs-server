---
layout: default-layout
title: class TextRemovedBinaryImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: text removed binary image, java
needAutoGenerateSidebar: true
---

# TextRemovedBinaryImageUnit

The `TextRemovedBinaryImageUnit` class represents an intermediate result unit that contains a text-removed binary image.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextRemovedBinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the text-removed binary image. |
| [`setImageData`](#setimagedata) | Sets the text-removed binary image. |

### getImageData

Gets the text-removed binary image.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the text-removed binary image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the text-removed binary image.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

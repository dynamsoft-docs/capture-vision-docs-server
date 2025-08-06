---
layout: default-layout
title: class ColourImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class ColourImageUnit in Dynamsoft Core Module.
keywords: colour image, java
needAutoGenerateSidebar: true
---

# ColourImageUnit

The `ColourImageUnit` class represents a unit that contains color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Package:* `com.dynamsoft.core.intermediate_results`

```java
class ColourImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the image data of the color image unit. |
| [`setImageData`](#setimagedata) | Sets the image data of the color image unit. |

### getImageData

Gets the image data of the color image unit.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the image data of the color image unit.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the image data of the color image unit.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exceptions**

[`CoreException`]({{ site.dcvb_java_api }}core/exceptions/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

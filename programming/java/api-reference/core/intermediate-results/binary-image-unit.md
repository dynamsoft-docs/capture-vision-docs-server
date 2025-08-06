---
layout: default-layout
title: class BinaryImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class BinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, java
needAutoGenerateSidebar: true
---

# BinaryImageUnit

The `BinaryImageUnit` class represents a unit that contains a binary image. It inherits from the `IntermediateResultUnit` class and stores binary image data.

## Definition

*Package:* `com.dynamsoft.core.intermediate_results`

```java
class BinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the binary image data. |
| [`setImageData`](#setimagedata) | Sets the binary image data. |

### getImageData

Gets the binary image data.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object containing the binary image data.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the binary image data.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exceptions**

[`CoreException`]({{ site.dcvb_java_api }}core/exceptions/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

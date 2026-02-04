---
layout: default-layout
title: class ScaledColourImageUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class ScaledColourImageUnit in Dynamsoft Core Module.
keywords: scaled colour image, java
needAutoGenerateSidebar: true
---

# ScaledColourImageUnit

The `ScaledColourImageUnit` class represents an intermediate result unit that contains scaled  color image. It is derived from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class ScaledColourImageUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getImageData`](#getimagedata) | Gets the image data of the unit.|
| [`setImageData`](#setimagedata) | Sets the image data of the unit. |

### getImageData

Gets the image data of the unit.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the image data of the unit.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageData

Sets the image data of the unit.

```java
void setImageData(ImageData imgData) throws CoreException
```

**Parameters**

`imgData` The image data to set.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

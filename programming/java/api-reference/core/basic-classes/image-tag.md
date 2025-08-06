---
layout: default-layout
title: ImageTag Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of ImageTag class in Dynamsoft Core Module Java Edition.
keywords: image tag, java
needAutoGenerateSidebar: true
---

# ImageTag

The `ImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
public abstract class ImageTag
```

## Attributes

| Attribute               | Type | Description |
|-------------------------|------|-------------|
| [`imageId`](#imageid) | *int* | The ID of the image. |
| [`mode`](#mode) | *int* | The capture distance mode of the image. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageTag`](#imagetag) | Constructor. Initializes a new instance of the `ImageTag` class. |
| [`getType`](#gettype) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |
| [`getImageId`](#getimageid) | Gets the ID of the image. |
| [`setImageId`](#setimageid) | Sets the ID of the image. |
| [`getImageCaptureDistanceMode`](#getimagecapturedistancemode) | Gets the capture distance mode of the image. |
| [`setImageCaptureDistanceMode`](#setimagecapturedistancemode) | Sets the capture distance mode of the image. |

## Attributes

### imageId

The ID of the image.

```java
int imageId
```

### mode

The capture distance mode of the image.

```java
@EnumImageCaptureDistanceMode int mode
```

## Methods

### ImageTag

Constructor. Initializes a new instance of the `ImageTag` class.

```java
protected ImageTag()
```

### getType

Gets the type of the image tag.

```java
public abstract @EnumImageTagType int getType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_java_api }}core/enum-image-tag-type.html)

### clone

Creates a copy of the image tag.

```java
public abstract ImageTag clone()
```

**Return Value**

Returns a copy of the image tag.

### getImageId

Gets the ID of the image.

```java
int getImageId()
```

**Return Value**

Returns the ID of the image.

### setImageId

Sets the ID of the image.

```java
void setImageId(int imageId)
```

**Parameters**

`imageId` The ID of the image.

### getImageCaptureDistanceMode

Gets the capture distance mode of the image.

```java
@EnumImageCaptureDistanceMode int getImageCaptureDistanceMode()
```

**Return Value**

Returns the capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_java_api }}core/enum-image-capture-distance-mode.html)

### setImageCaptureDistanceMode

Sets the capture distance mode of the image.

```java
void setImageCaptureDistanceMode(@EnumImageCaptureDistanceMode int mode)
```

**Parameters**

`mode` The capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_java_api }}core/enum-image-capture-distance-mode.html)

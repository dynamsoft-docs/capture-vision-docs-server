---
layout: default-layout
title: VideoFrameTag Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of VideoFrameTag class in Dynamsoft Core Module Java Edition.
keywords: video frame tag, java
needAutoGenerateSidebar: true
---

# VideoFrameTag

The `VideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `ImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class VideoFrameTag extends ImageTag
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`quality`](#quality) | *int* | The quality of the video frame. |
| [`isCropped`](#iscropped) | *boolean* | A boolean value indicating whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | *Rect* | The crop region of the video frame. |
| [`originalWidth`](#originalwidth) | *int* | The original width of the video frame. |
| [`originalHeight`](#originalheight) | *int* | The original height of the video frame. |

## Constructors

| Constructor | Description |
|-------------|-------------|
| [`VideoFrameTag`](#videoframetag) | Initializes a new instance of the `VideoFrameTag` class. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getVideoFrameQuality`](#getvideoframequality) | Gets the quality of the video frame.|
| [`isCropped`](#iscropped-method) | Determines whether the video frame is cropped. |
| [`getCropRegion`](#getcropregion) | Gets the crop region of the video frame. |
| [`getOriginalWidth`](#getoriginalwidth) | Gets the original width of the video frame. |
| [`getOriginalHeight`](#getoriginalheight) | Gets the original height of the video frame. |
| [`getType`](#gettype) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |

## Attributes

### quality

The quality of the video frame.

```java
protected @EnumVideoFrameQuality int quality
```

### isCropped

A boolean value indicating whether the video frame is cropped.

```java
public boolean isCropped
```

### cropRegion

The crop region of the video frame.

```java
public Rect cropRegion
```

### originalWidth

The original width of the video frame.

```java
public int originalWidth
```

### originalHeight

The original height of the video frame.

```java
public int originalHeight
```

## Constructors

### VideoFrameTag

Initializes a new instance of the `VideoFrameTag` class.

```java
VideoFrameTag(@EnumVideoFrameQuality int quality, boolean isCropped, Rect cropRegion, int originalWidth, int originalHeight)
```

**Parameters**

`quality` The quality of the video frame.

`isCropped` A boolean value indicating whether the video frame is cropped.

`cropRegion` A `Rect` object that represents the crop region of the video frame.

`originalWidth` The original width of the video frame.

`originalHeight` The original height of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcvb_java_api }}core/enum-video-frame-quality.html)

## Methods

### getVideoFrameQuality

Gets the quality of the video frame.

```java
@EnumVideoFrameQuality int getVideoFrameQuality()
```

**Return Value**

Returns the quality of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcvb_java_api }}core/enum-video-frame-quality.html)

### isCropped

Determines whether the video frame is cropped.

```java
boolean isCropped()
```

**Return Value**

Returns true if the video frame is cropped, false otherwise.

### getCropRegion

Gets the crop region of the video frame.

```java
Rect getCropRegion()
```

**Return Value**

Returns a `Rect` object that represents the crop region of the video frame. It may be null.

**See Also**

[Rect]({{ site.dcvb_java_api }}core/basic-classes/rect.html)

### getOriginalWidth

Gets the original width of the video frame.

```java
int getOriginalWidth()
```

**Return Value**

Returns the original width of the video frame.

### getOriginalHeight

Gets the original height of the video frame.

```java
int getOriginalHeight()
```

**Return Value**

Returns the original height of the video frame.

### getType

Gets the type of the image tag.

```java
@EnumImageTagType int getType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_java_api }}core/enum-image-tag-type.html)

### clone

Creates a copy of the image tag.

```java
VideoFrameTag clone()
```

**Return Value**

Returns a copy of the `VideoFrameTag` object.

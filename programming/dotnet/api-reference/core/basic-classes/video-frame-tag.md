---
layout: default-layout
title: VideoFrameTag Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of VideoFrameTag class in Dynamsoft Core Module .NET Edition.
keywords: video frame tag, .NET
needAutoGenerateSidebar: true
---

# VideoFrameTag

The `VideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `ImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public class VideoFrameTag : ImageTag 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetVideoFrameQuality`](#getvideoframequality) | Gets the quality of the video frame.|
| [`IsCropped`](#iscropped) | Determines whether the video frame is cropped. |
| [`GetCropRegion`](#getcropregion) | Gets the crop region of the video frame. |
| [`GetOriginalWidth`](#getoriginalwidth) | Gets the original width of the video frame. |
| [`GetOriginalHeight`](#getoriginalheight) | Gets the original height of the video frame. |
| [`VideoFrameTag`](#VideoFrameTag-constructor) | The constructor of the `VideoFrameTag` class. |
| [`GetImageTagType`](#getimagetagtype) | Gets the type of the image tag. |
| [`Clone`](#clone) | Creates a copy of the image tag. |

### GetVideoFrameQuality

Gets the quality of the video frame.

```csharp
EnumVideoFrameQuality GetVideoFrameQuality()
```

**Return Value**

Returns the quality of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcv_enumerations }}core/video-frame-quality.html?lang=dotnet)

### IsCropped

Determines whether the video frame is cropped.

```csharp
bool IsCropped()
```

**Return Value**

Returns true if the video frame is cropped, false otherwise.

### GetCropRegion

Gets the crop region of the video frame.

```csharp
Rect GetCropRegion()
```

**Return Value**

Returns a `Rect` object that represents the crop region of the video frame. It may be null.

**See Also**

[Rect]({{ site.dcv_dotnet_api }}core/basic-classes/rect.html)

### GetOriginalWidth

Gets the original width of the video frame.

```csharp
int GetOriginalWidth()
```

**Return Value**

Returns the original width of the video frame.

### GetOriginalHeight

Gets the original height of the video frame.

```csharp
int GetOriginalHeight()
```

**Return Value**

Returns the original height of the video frame.

### VideoFrameTag Constructor

The constructor of the `VideoFrameTag` class.

```csharp
VideoFrameTag(EnumVideoFrameQuality quality, bool isCropped, Rect cropRegion, int originalWidth, int originalHeight)
```

**Parameters**

`[in] quality` The quality of the video frame.

`[in] isCropped` A boolean value indicating whether the video frame is cropped.

`[in] cropRegion` A `Rect` object that represents the crop region of the video frame.

`[in] originalWidth` The original width of the video frame.

`[in] originalHeight` The original height of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcv_enumerations }}core/video-frame-quality.html?lang=dotnet)

### GetImageTagType

Gets the type of the image tag.

```csharp
EnumImageTagType GetImageTagType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcv_enumerations }}core/image-tag-type.html?lang=dotnet)

### Clone

Creates a copy of the image tag.

```csharp
ImageTag Clone()
```

**Return Value**

Returns a copy of the image tag.

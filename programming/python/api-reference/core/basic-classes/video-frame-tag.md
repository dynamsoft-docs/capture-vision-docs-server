---
layout: default-layout
title: VideoFrameTag Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of VideoFrameTag class in Dynamsoft Core Module Python Edition.
keywords: video frame tag, python
needAutoGenerateSidebar: true
---

# VideoFrameTag

The `VideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `ImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Module:* dynamsoft_core

```python
class VideoFrameTag(ImageTag) 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `VideoFrameTag` class. |
| [`get_video_frame_quality`](#get_video_frame_quality) | Gets the quality of the video frame.|
| [`is_cropped`](#is_cropped) | Determines whether the video frame is cropped. |
| [`get_crop_region`](#get_crop_region) | Gets the crop region of the video frame. |
| [`get_original_width`](#get_original_width) | Gets the original width of the video frame. |
| [`get_original_height`](#get_original_height) | Gets the original height of the video frame. |
| [`VideoFrameTag`](#VideoFrameTag-constructor) | The constructor of the `VideoFrameTag` class. |
| [`get_type`](#get_type) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |

### \_\_init\_\_

Initializes a new instance of the `VideoFrameTag` class.

```python
def __init__(self, quality: int, is_cropped: bool, crop_region: "Rect", original_width: int, original_height: int):
```

**Parameters**

`quality` The quality of the video frame.

`is_cropped` A boolean value indicating whether the video frame is cropped.

`crop_region` A `Rect` object that represents the crop region of the video frame.

`original_width` The original width of the video frame.

`original_height` The original height of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcvb_python_api }}core/enum-video-frame-quality.html)

### get_video_frame_quality

Gets the quality of the video frame.

```python
def get_video_frame_quality(self) -> int:
```

**Return Value**

Returns the quality of the video frame.

**See Also**

[EnumVideoFrameQuality]({{ site.dcvb_python_api }}core/enum-video-frame-quality.html)

### is_cropped

Determines whether the video frame is cropped.

```python
def is_cropped(self) -> bool:
```

**Return Value**

Returns true if the video frame is cropped, false otherwise.

### get_crop_region

Gets the crop region of the video frame.

```python
def get_crop_region(self) -> Rect:
```

**Return Value**

Returns a `Rect` object that represents the crop region of the video frame. It may be null.

**See Also**

[Rect]({{ site.dcvb_python_api }}core/basic-classes/rect.html)

### get_original_width

Gets the original width of the video frame.

```python
def get_original_width(self) -> int:
```

**Return Value**

Returns the original width of the video frame.

### get_original_height

Gets the original height of the video frame.

```python
def get_original_height(self) -> int:
```

**Return Value**

Returns the original height of the video frame.

### get_type

Gets the type of the image tag.

```python
def get_type(self) -> int:
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_python_api }}core/enum-image-tag-type.html)

### clone

Creates a copy of the image tag.

```python
def clone(self) -> "VideoFrameTag":
```

**Return Value**

Returns a copy of the `VideoFrameTag` object.

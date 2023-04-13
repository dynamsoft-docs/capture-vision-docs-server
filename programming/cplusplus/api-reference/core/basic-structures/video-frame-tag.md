---
layout: default-layout
title: class CVideoFrameTag - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CVideoFrameTag in Dynamsoft Core Module.
keywords: video frame tag, c++
needAutoGenerateSidebar: true
---

# CVideoFrameTag

The CVideoFrameTag class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the CImageTag class and adds additional attributes and methods specific to video frames.

```cpp
class dynamsoft::core::basic_structures::CVideoFrameTag: public CImageTag 
```

---

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetVideoFrameQuality`](#getvideoframequality) | It is used to get the quality of the video frame.|
| [`IsCropped`](#iscropped) | It is used to determine whether the video frame is cropped. |
| [`GetCropRegion`](#getcropregion) | It is used to get the crop region of the video frame. |
| [`GetOriginalWidth`](#getoriginalwidth) | It is used to get the original width of the video frame. |
| [`GetOriginalHeight`](#getoriginalheight) | It is used to get the original height of the video frame. |
| [`CVideoFrameTag`](#cvideoframetag-constructor) | The constructor of the CVideoFrameTag class. |
| [`~CVideoFrameTag`](#cvideoframetag-destructor) | The destructor of the CVideoFrameTag class. |

### GetVideoFrameQuality

It is used to get the quality of the video frame.

```cpp
VideoFrameQuality GetVideoFrameQuality() const
```

**Return value**

Returns the quality of the video frame.

### IsCropped

It is used to determine whether the video frame is cropped.

```cpp
bool IsCropped() const
```

**Return value**

Returns true if the video frame is cropped, false otherwise.

### GetCropRegion

It is used to get the crop region of the video frame.

```cpp
const CRect* GetCropRegion() const
```

**Return value**

Returns a pointer to a CRect object that represents the crop region of the video frame. It may be NULL.

### GetOriginalWidth

It is used to get the original width of the video frame.

```cpp
int GetOriginalWidth() const
```

**Return value**

Returns the original width of the video frame.

### GetOriginalHeight

It is used to get the original height of the video frame.

```cpp
int GetOriginalHeight() const
```

**Return value**

Returns the original height of the video frame.

### CVideoFrameTag Constructor

The constructor of the CVideoFrameTag class.

```cpp
CVideoFrameTag(VideoFrameQuality quality, bool isCropped, const CRect* cropRegion, int originalWidth, int originalHidth)
```

**Parameters**

`[in] quality` The quality of the video frame.

`[in] isCropped` A boolean value indicating whether the video frame is cropped.

`[in] cropRegion` A pointer to a CRect object that represents the crop region of the video frame.

`[in] originalWidth` The original width of the video frame.

`[in] originalHeight` The original height of the video frame.

### CVideoFrameTag Destructor

The destructor of the CVideoFrameTag class.

```cpp
virtual ~CVideoFrameTag()
```

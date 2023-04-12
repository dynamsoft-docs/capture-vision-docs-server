---
layout: default-layout
title: class CImageTag - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageTag in Dynamsoft Core Module.
keywords: image tag, c++
needAutoGenerateSidebar: true
---

# CImageTag

The CImageTag class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

```cpp
class dynamsoft::core::basic_structures::CImageTag 
```

---

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetType`](#gettype) | It is used to get the type of the image tag. |
| [`Clone`](#clone) | It is used to create a copy of the image tag. |
| [`GetImageId`](#getimageid) | It is used to get the ID of the image. |
| [`SetImageId`](#setimageid) | It is used to set the ID of the image. |
| [`GetImageCaptureDistanceMode`](#getimagecapturedistancemode) | It is used to get the capture distance mode of the image. |
| [`SetImageCaptureDistanceMode`](#setimagecapturedistancemode) | It is used to set the capture distance mode of the image. |

### GetType

It is used to get the type of the image tag.

```cpp
virtual ImageTagType GetType() const
```

**Return value**

Returns the type of the image tag.

### Clone

It is used to create a copy of the image tag.

```cpp
virtual CImageTag* Clone() const
```

**Return value**

Returns a pointer to a copy of the image tag.

### GetImageId

It is used to get the ID of the image.

```cpp
int GetImageId() const
```

**Return value**

Returns the ID of the image.

### SetImageId

It is used to set the ID of the image.

```cpp
void SetImageId(int imgId)
```

**Parameters**

`[in] imgId` The ID of the image.

### GetImageCaptureDistanceMode

It is used to get the capture distance mode of the image.

```cpp
ImageCaptureDistanceMode GetImageCaptureDistanceMode() const
```

**Return value**

Returns the capture distance mode of the image.

### SetImageCaptureDistanceMode

It is used to set the capture distance mode of the image.

```cpp
void SetImageCaptureDistanceMode(ImageCaptureDistanceMode mode)
```

**Parameters**

`[in] mode` The capture distance mode of the image.

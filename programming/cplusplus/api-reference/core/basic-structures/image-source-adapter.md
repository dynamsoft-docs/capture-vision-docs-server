---
layout: default-layout
title: class CImageSourceAdapter - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageSourceAdapter in Dynamsoft Core Module.
keywords: image source adapter, c++
needAutoGenerateSidebar: true
---

# CImageSourceAdapter

The `CImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CImageSourceAdapter 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`AddImageToBuffer`](#addimagetobuffer) | Adds an image to the buffer of the adapter. |
| [`HasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`StartFetching`](#startfetching) | Starts fetching images. |
| [`StopFetching`](#stopfetching) | Stops fetching images. |
| [`GetImage`](#getimage) | Returns a buffered image. |
| [`SetMaxImageCount`](#setmaximagecount) | Sets how many images are allowed to be buffered. |
| [`GetMaxImageCount`](#getmaximagecount) | Returns how many images can be buffered. |
| [`SetBufferOverflowProtectionMode`](#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [`GetBufferOverflowProtectionMode`](#getbufferoverflowprotectionmode) | Returns the current buffer overflow protection mode. |
| [`HasImage`](#hasimage) | Determines whether the image is in the buffer or not. |
| [`SetNextImageToReturn`](#setnextimagetoreturn) | Sets the next image to return. |
| [`GetImageCount`](#getimagecount) | Returns the actual count of buffered images. |
| [`IsBufferEmpty`](#isbufferempty) | Determines whether the buffer is empty. |
| [`ClearBuffer`](#clearbuffer) | Clears the image buffer. |
| [`SetColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type of a color channel in an image. |
| [`GetColourChannelUsageType`](#getcolourchannelusagetype) | Gets the usage type of a color channel in an image. |
| [`SetErrorListener`](#seterrorlistener) | Sets the error listener for the image source. |


### AddImageToBuffer

Adds an image to the buffer of the adapter.

```cpp
void AddImageToBuffer(const CImageData* img, bool bClone = true);
```

**Parameters**

`[in] img` The image to add to the buffer.

`[in] bClone` Whether the image should be cloned before being added to the buffer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### HasNextImageToFetch

Determines whether there are more images left to fetch.

```cpp
virtual bool HasNextImageToFetch() const;
```

**Return value**

Returns true if there are more images left to fetch, false otherwise. This function must be implemented in the subclass.

### StartFetching

Starts fetching images.

```cpp
virtual void StartFetching();
```

### StopFetching

Stops fetching images.

```cpp
virtual void StopFetching();
```

### GetImage

Returns a buffered image.

```cpp
virtual CImageData* GetImage();
```

**Return value**

Returns a pointer to the image if it exists in the buffer, NULL otherwise.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetMaxImageCount

Sets how many images are allowed to be buffered.

```cpp
void SetMaxImageCount(int count);
```

**Parameters**

`[in] count` The maximum number of images that can be buffered.

### GetMaxImageCount

Returns how many images can be buffered.

```cpp
int GetMaxImageCount() const;
```

**Return value**

Returns the maximum number of images that can be buffered.

### SetBufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full.

```cpp
void SetBufferOverflowProtectionMode(BufferOverflowProtectionMode mode);
```

**Parameters**

`[in] mode` The buffer overflow protection mode to set.

**See Also**

[BufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)

### GetBufferOverflowProtectionMode

Returns the current buffer overflow protection mode.

```cpp
BufferOverflowProtectionMode GetBufferOverflowProtectionMode() const;
```

**Return value**

Returns the current buffer overflow protection mode.

**See Also**

[BufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)

### HasImage

Determines whether the image is in the buffer or not.

```cpp
bool HasImage(int imageId) const;
```

**Parameters**

`[in] imageId` The ID of the image to check.

**Return value**

Returns true if the image is in the buffer, false otherwise.

### SetNextImageToReturn

Sets the next image to return.

```cpp
bool SetNextImageToReturn(int imageId, bool keepInBuffer = true);
```

**Parameters**

`[in] imageId` The ID of the next image to return.

`[in] keepInBuffer` Whether the image should be retained in the buffer, even if the buffer is full and the image needs to be updated based on the `BufferOverflowProtectionMode` parameter.

**Return value**

Returns true if the image is in the buffer and is set as the next image to return, false otherwise.

### GetImageCount

Returns the actual count of buffered images.

```cpp
int GetImageCount() const;
```

**Return value**

Returns the actual count of buffered images.

### IsBufferEmpty

Determines whether the buffer is empty.

```cpp
bool IsBufferEmpty() const;
```

**Return value**

Returns true if the buffer is empty, false otherwise.

### ClearBuffer

Clear the image buffer.

```cpp
void ClearBuffer();
```

### SetColourChannelUsageType

Sets the usage type of a color channel in images.

```cpp
void SetColourChannelUsageType(ColourChannelUsageType type);
```

**Parameters**

`[in] type` The usage type of a color channel in images to set.

**See Also**

[ColourChannelUsageType]({{ site.dcvb_enumerations}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)

### GetColourChannelUsageType

Gets the usage type of a color channel in images.

```cpp
ColourChannelUsageType GetColourChannelUsageType() const;
```

**Return value**

Returns the usage type of a color channel in images.

**See Also**

[ColourChannelUsageType]({{ site.dcvb_enumerations}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)

### SetErrorListener

This function allows you to set an error listener object that will receive notifications when errors occur during image source operations. If an error occurs, the error infomation will be passed to the listener's `OnErrorReceived` method.

```cpp
void SetErrorListener(CImageSourceErrorListener* listener);
```

**Parameters**

`[in] listener` A pointer to an instance of `CImageSourceErrorListener` or its derived class, which will handle error notifications.

**See Also**

[CImageSourceErrorListener]({{ site.dcvb_cpp_api }}core/basic-structures/image-source-error-listener.html)

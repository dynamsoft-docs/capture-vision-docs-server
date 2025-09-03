---
layout: default-layout
title: ImageSourceAdapter Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of ImageSourceAdapter class in Dynamsoft Core Module .NET Edition.
keywords: image source adapter, .NET
needAutoGenerateSidebar: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public abstract class ImageSourceAdapter 
```

## Methods

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
| [`Dispose`](#dispose) | Releases all resources used by current object. |


### AddImageToBuffer

Adds an image to the buffer of the adapter.

```csharp
void AddImageToBuffer(ImageData img)
```

**Parameters**

`[in] img` The image to add to the buffer.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### HasNextImageToFetch

Determines whether there are more images left to fetch.

```csharp
abstract bool HasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise. This function must be implemented in the subclass.

### StartFetching

Starts fetching images.

```csharp
virtual void StartFetching()
```

### StopFetching

Stops fetching images.

```csharp
virtual void StopFetching()
```

### GetImage

Returns a buffered image.

```csharp
virtual ImageData GetImage()
```

**Return Value**

Returns an image if it exists in the buffer, null otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetMaxImageCount

Sets how many images are allowed to be buffered.

```csharp
void SetMaxImageCount(int count)
```

**Parameters**

`[in] count` The maximum number of images that can be buffered.

### GetMaxImageCount

Returns how many images can be buffered.

```csharp
int GetMaxImageCount()
```

**Return Value**

Returns the maximum number of images that can be buffered.

### SetBufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full.

```csharp
void SetBufferOverflowProtectionMode(EnumBufferOverflowProtectionMode mode)
```

**Parameters**

`[in] mode` The buffer overflow protection mode to set.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=dotnet)

### GetBufferOverflowProtectionMode

Returns the current buffer overflow protection mode.

```csharp
EnumBufferOverflowProtectionMode GetBufferOverflowProtectionMode()
```

**Return Value**

Returns the current buffer overflow protection mode.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=dotnet)

### HasImage

Determines whether the image is in the buffer or not.

```csharp
bool HasImage(int imageId)
```

**Parameters**

`[in] imageId` The ID of the image to check.

**Return Value**

Returns true if the image is in the buffer, false otherwise.

### SetNextImageToReturn

Sets the next image to return.

```csharp
bool SetNextImageToReturn(int imageId, bool keepInBuffer = true)
```

**Parameters**

`[in] imageId` The ID of the next image to return.

`[in] keepInBuffer` Whether the image should be retained in the buffer, even if the buffer is full and the image needs to be updated based on the `BufferOverflowProtectionMode` parameter.

**Return Value**

Returns true if the image is in the buffer and is set as the next image to return, false otherwise.

### GetImageCount

Returns the actual count of buffered images.

```csharp
int GetImageCount()
```

**Return Value**

Returns the actual count of buffered images.

### IsBufferEmpty

Determines whether the buffer is empty.

```csharp
bool IsBufferEmpty()
```

**Return Value**

Returns true if the buffer is empty, false otherwise.

### ClearBuffer

Clear the image buffer.

```csharp
void ClearBuffer()
```

### SetColourChannelUsageType

Sets the usage type of a color channel in images.

```csharp
void SetColourChannelUsageType(EnumColourChannelUsageType type)
```

**Parameters**

`[in] type` The usage type of a color channel in images to set.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_enumerations}}core/colour-channel-usage-type.html?lang=dotnet)

### GetColourChannelUsageType

Gets the usage type of a color channel in images.

```csharp
EnumColourChannelUsageType GetColourChannelUsageType()
```

**Return Value**

Returns the usage type of a color channel in images.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_enumerations}}core/colour-channel-usage-type.html?lang=dotnet)

### SetErrorListener

This function allows you to set an error listener object that will receive notifications when errors occur during image source operations. If an error occurs, the error infomation will be passed to the listener's `OnErrorReceived` method.

```csharp
void SetErrorListener(IImageSourceErrorListener listener)
```

**Parameters**

`[in] listener` Specifies a listening object of the type `IImageSourceErrorListener`, which will handle error notifications.

**See Also**

[IImageSourceErrorListener]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-error-listener.html)


### Dispose

Releases all resources used by current object.

```csharp
void Dispose()
```

---
layout: default-layout
title: ImageSourceAdapter Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of ImageSourceAdapter class in Dynamsoft Core Module Java Edition.
keywords: image source adapter, java
needAutoGenerateSidebar: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an class for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

>Note: Subclasses inheriting from this class must ensure that the parent class constructor (`super()`) is properly called to guarantee correct initialization.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
public abstract class ImageSourceAdapter
```

## Methods

| Method | Description |
|--------|-------------|
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the buffer of the adapter. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`startFetching`](#startfetching) | Starts fetching images. |
| [`stopFetching`](#stopfetching) | Stops fetching images. |
| [`getImage`](#getimage) | Returns a buffered image. |
| [`setMaxImageCount`](#setmaximagecount) | Sets how many images are allowed to be buffered. |
| [`getMaxImageCount`](#getmaximagecount) | Returns how many images can be buffered. |
| [`setBufferOverflowProtectionMode`](#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [`getBufferOverflowProtectionMode`](#getbufferoverflowprotectionmode) | Returns the current buffer overflow protection mode. |
| [`hasImage`](#hasimage) | Determines whether the image is in the buffer or not. |
| [`setNextImageToReturn`](#setnextimagetoreturn) | Sets the next image to return. |
| [`getImageCount`](#getimagecount) | Returns the actual count of buffered images. |
| [`isBufferEmpty`](#isbufferempty) | Determines whether the buffer is empty. |
| [`clearBuffer`](#clearbuffer) | Clears the image buffer. |
| [`setColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type of a color channel in an image. |
| [`getColourChannelUsageType`](#getcolourchannelusagetype) | Gets the usage type of a color channel in an image. |
| [`setErrorListener`](#seterrorlistener) | Sets the error listener for the image source. |


### addImageToBuffer

Adds an image to the buffer of the adapter.

```java
void addImageToBuffer(ImageData img)
```

**Parameters**

`img` The image to be added to the buffer.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### hasNextImageToFetch

Determines whether there are more images left to fetch.

```java
public abstract boolean hasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise. This function must be implemented in the subclass.

### startFetching

Starts fetching images.

```java
void startFetching()
```

### stopFetching

Stops fetching images.

```java
void stopFetching()
```

### getImage

Returns a buffered image.

```java
ImageData getImage()
```

**Return Value**

Returns an image if it exists in the buffer, null otherwise.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setMaxImageCount

Sets how many images are allowed to be buffered.

```java
void setMaxImageCount(int count)
```

**Parameters**

`count` The maximum number of images that can be buffered.

### getMaxImageCount

Returns how many images can be buffered.

```java
int getMaxImageCount()
```

**Return Value**

Returns the maximum number of images that can be buffered.

### setBufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full.

```java
void setBufferOverflowProtectionMode(@EnumBufferOverflowProtectionMode int mode)
```

**Parameters**

`mode` The buffer overflow protection mode to set.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_java_api }}core/enum-buffer-overflow-protection-mode.html)

### getBufferOverflowProtectionMode

Returns the current buffer overflow protection mode.

```java
@EnumBufferOverflowProtectionMode int getBufferOverflowProtectionMode()
```

**Return Value**

Returns the current buffer overflow protection mode.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_java_api }}core/enum-buffer-overflow-protection-mode.html)

### hasImage

Determines whether the image is in the buffer or not.

```java
boolean hasImage(int imageId)
```

**Parameters**

`imageId` The ID of the image to check.

**Return Value**

Returns true if the image is in the buffer, false otherwise.

### setNextImageToReturn

Sets the next image to return.

```java
boolean setNextImageToReturn(int imageId, boolean keepInBuffer)
```

**Parameters**

`imageId` The ID of the next image to return.

`keepInBuffer` Whether the image should be retained in the buffer, even if the buffer is full and the image needs to be updated based on the `BufferOverflowProtectionMode` parameter.

**Return Value**

Returns true if the image is in the buffer and is set as the next image to return, false otherwise.

### getImageCount

Returns the actual count of buffered images.

```java
int getImageCount()
```

**Return Value**

Returns the actual count of buffered images.

### isBufferEmpty

Determines whether the buffer is empty.

```java
boolean isBufferEmpty()
```

**Return Value**

Returns true if the buffer is empty, false otherwise.

### clearBuffer

Clear the image buffer.

```java
void clearBuffer()
```

### setColourChannelUsageType

Sets the usage type of a color channel in images.

```java
void setColourChannelUsageType(@EnumColourChannelUsageType int type)
```

**Parameters**

`type` The usage type of a color channel in images to set.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_java_api }}core/enum-colour-channel-usage-type.html)

### getColourChannelUsageType

Gets the usage type of a color channel in images.

```java
@EnumColourChannelUsageType int getColourChannelUsageType()
```

**Return Value**

Returns the usage type of a color channel in images.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_java_api }}core/enum-colour-channel-usage-type.html)

### setErrorListener

This function allows you to set an error listener object that will receive notifications when errors occur during image source operations. If an error occurs, the error infomation will be passed to the listener's `onErrorReceived` method.

```java
void setErrorListener(ImageSourceErrorListener listener)
```

**Parameters**

`listener` Specifies a listening object of the type `ImageSourceErrorListener`, which will handle error notifications.

**See Also**

[ImageSourceErrorListener]({{ site.dcvb_java_api }}core/basic-classes/image-source-error-listener.html)

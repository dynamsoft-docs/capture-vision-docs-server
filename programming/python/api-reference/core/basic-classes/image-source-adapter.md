---
layout: default-layout
title: ImageSourceAdapter Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of ImageSourceAdapter class in Dynamsoft Core Module Python Edition.
keywords: image source adapter, python
needAutoGenerateSidebar: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an class for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Module:* dynamsoft_core

```python
class ImageSourceAdapter(ABC) 
```

## Methods

| Method | Description |
|--------|-------------|
| [`add_image_to_buffer`](#add_image_to_buffer) | Adds an image to the buffer of the adapter. |
| [`has_next_image_to_fetch`](#has_next_image_to_fetch) | Determines whether there are more images left to fetch. |
| [`start_fetching`](#start_fetching) | Starts fetching images. |
| [`stop_fetching`](#stop_fetching) | Stops fetching images. |
| [`get_image`](#get_image) | Returns a buffered image. |
| [`set_max_image_count`](#set_max_image_count) | Sets how many images are allowed to be buffered. |
| [`get_max_image_count`](#get_max_image_count) | Returns how many images can be buffered. |
| [`set_buffer_overflow_protection_mode`](#set_buffer_overflow_protection_mode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. |
| [`get_buffer_overflow_protection_mode`](#get_buffer_overflow_protection_mode) | Returns the current buffer overflow protection mode. |
| [`has_image`](#has_image) | Determines whether the image is in the buffer or not. |
| [`set_next_image_to_return`](#set_next_image_to_return) | Sets the next image to return. |
| [`get_image_count`](#get_image_count) | Returns the actual count of buffered images. |
| [`is_buffer_empty`](#is_buffer_empty) | Determines whether the buffer is empty. |
| [`clear_buffer`](#clear_buffer) | Clears the image buffer. |
| [`set_colour_channel_usage_type`](#set_colour_channel_usage_type) | Sets the usage type of a color channel in an image. |
| [`get_colour_channel_usage_type`](#get_colour_channel_usage_type) | Gets the usage type of a color channel in an image. |
| [`set_error_listener`](#set_error_listener) | Sets the error listener for the image source. |


### add_image_to_buffer

Adds an image to the buffer of the adapter.

```python
def add_image_to_buffer(self, image: ImageData) -> None:
```

**Parameters**

`image` The image to be added to the buffer.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### has_next_image_to_fetch

Determines whether there are more images left to fetch.

```python
@abstractmethod
def has_next_image_to_fetch(self) -> bool:
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise. This function must be implemented in the subclass.

### start_fetching

Starts fetching images.

```python
def start_fetching(self) -> None:
```

### stop_fetching

Stops fetching images.

```python
def stop_fetching(self) -> None:
```

### get_image

Returns a buffered image.

```python
def get_image(self) -> ImageData:
```

**Return Value**

Returns an image if it exists in the buffer, null otherwise.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

### set_max_image_count

Sets how many images are allowed to be buffered.

```python
def set_max_image_count(self, count: int) -> None:
```

**Parameters**

`count` The maximum number of images that can be buffered.

### get_max_image_count

Returns how many images can be buffered.

```python
def get_max_image_count(self) -> int:
```

**Return Value**

Returns the maximum number of images that can be buffered.

### set_buffer_overflow_protection_mode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full.

```python
def set_buffer_overflow_protection_mode(self, mode: int) -> None:
```

**Parameters**

`mode` The buffer overflow protection mode to set.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=python)

### get_buffer_overflow_protection_mode

Returns the current buffer overflow protection mode.

```python
def get_buffer_overflow_protection_mode(self) -> int:
```

**Return Value**

Returns the current buffer overflow protection mode.

**See Also**

[EnumBufferOverflowProtectionMode]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=python)

### has_image

Determines whether the image is in the buffer or not.

```python
def has_image(self, image_id: int) -> bool:
```

**Parameters**

`image_id` The ID of the image to check.

**Return Value**

Returns true if the image is in the buffer, false otherwise.

### set_next_image_to_return

Sets the next image to return.

```python
def set_next_image_to_return(self, image_id: int, keep_in_buffer: bool = True) -> bool:
```

**Parameters**

`image_id` The ID of the next image to return.

`keep_in_buffer` Whether the image should be retained in the buffer, even if the buffer is full and the image needs to be updated based on the `BufferOverflowProtectionMode` parameter.

**Return Value**

Returns true if the image is in the buffer and is set as the next image to return, false otherwise.

### get_image_count

Returns the actual count of buffered images.

```python
def get_image_count(self) -> int:
```

**Return Value**

Returns the actual count of buffered images.

### is_buffer_empty

Determines whether the buffer is empty.

```python
def is_buffer_empty(self) -> bool:
```

**Return Value**

Returns true if the buffer is empty, false otherwise.

### clear_buffer

Clear the image buffer.

```python
def clear_buffer(self) -> None:
```

### set_colour_channel_usage_type

Sets the usage type of a color channel in images.

```python
def set_colour_channel_usage_type(self, type: int) -> None:
```

**Parameters**

`type` The usage type of a color channel in images to set.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_enumerations }}core/colour-channel-usage-type.html?lang=python)

### get_colour_channel_usage_type

Gets the usage type of a color channel in images.

```python
def get_colour_channel_usage_type(self) -> int:
```

**Return Value**

Returns the usage type of a color channel in images.

**See Also**

[EnumColourChannelUsageType]({{ site.dcvb_enumerations }}core/colour-channel-usage-type.html?lang=python)

### set_error_listener

This function allows you to set an error listener object that will receive notifications when errors occur during image source operations. If an error occurs, the error infomation will be passed to the listener's `on_error_received` method.

```python
def set_error_listener(self, listener: ImageSourceErrorListener) -> None:
```

**Parameters**

`listener` Specifies a listening object of the type `ImageSourceErrorListener`, which will handle error notifications.

**See Also**

[ImageSourceErrorListener]({{ site.dcvb_python_api }}core/basic-classes/image-source-error-listener.html)

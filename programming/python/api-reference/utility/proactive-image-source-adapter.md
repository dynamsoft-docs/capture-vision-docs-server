---
layout: default-layout
title: ProactiveImageSourceAdapter Class - Dynamsoft Utility Module Python Edition API Reference
description: Definition of ProactiveImageSourceAdapter class in Dynamsoft Utility Module Python Edition.
keywords: proactive image source adapter, python
needAutoGenerateSidebar: true
---

# ProactiveImageSourceAdapter

The `ProactiveImageSourceAdapter` class is an abstract class that extends the `ImageSourceAdapter` class. It provides classs for proactively fetching images in a separate thread.

## Definition

*Module:* utility

*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_python_api }}core/basic-classes/image-source-adapter.html) -> ProactiveImageSourceAdapter

```python
class ProactiveImageSourceAdapter(ImageSourceAdapter, ABC):
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`_fetch_image`](#_fetch_image) | This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.|
| [`set_image_fetch_interval`](#set_image_fetch_interval) | Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`get_image_fetch_interval`](#get_image_fetch_interval) | Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`has_next_image_to_fetch`](#has_next_image_to_fetch) | Determines whether there are more images left to fetch. |
| [`start_fetching`](#start_fetching) | Starts fetching images. |
| [`stop_fetching`](#stop_fetching) | Stops fetching images. |

### _fetch_image

This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.

```python
@abstractmethod
def _fetch_image():
```

### set_image_fetch_interval

Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```python
def set_image_fetch_interval(self, milliseconds: int) -> None:
```

**Parameters**

- `milliseconds` Specifies the wait time in milliseconds. If setting to -1, the `ImageSource` does not proactively fetch images.

### get_image_fetch_interval

Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```python
def get_image_fetch_interval(self) -> int:
```

**Return Value**

Returns the wait time in milliseconds. If the value is -1, the `ImageSource` does not proactively fetch images.

### has_next_image_to_fetch

Determines whether there are more images left to fetch.

```python
def has_next_image_to_fetch(self) -> bool:
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

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

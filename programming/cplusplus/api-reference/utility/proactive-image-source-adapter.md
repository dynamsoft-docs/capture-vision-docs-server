---
layout: default-layout
title: class CProactiveImageSourceAdapter - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CProactiveImageSourceAdapter in Dynamsoft Utility Module.
keywords: proactive image source adapter, c++
needAutoGenerateSidebar: true
---

# CProactiveImageSourceAdapter

The CProactiveImageSourceAdapter class is an abstract base class that extends the CImageSourceAdapter class. It provides an interface for proactively fetching images in a separate thread.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CProactiveImageSourceAdapter: public CImageSourceAdapter
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`FetchImage`](#fetchimage) | This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.|
| [`SetImageFetchInterval`](#setimagefetchinterval) | Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |
| [`GetImageFetchInterval`](#getimagefetchinterval) | Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |

### FetchImage

This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.

```cpp
virtual CImageData* FetchImage() = 0;
```

**Return value**

Returns a pointer to the CImageData object representing the fetched image.

### SetImageFetchInterval

Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

```cpp
void SetImageFetchInterval(int milliseconds);
```

**Parameters**

- `[in] milliseconds` - Specifies the wait time in milliseconds. If set to -1, the ImageSource does not proactively fetch images.

### GetImageFetchInterval

Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

```cpp
int GetImageFetchInterval();
```

**Return value**

Returns the wait time in milliseconds. If the value is -1, the ImageSource does not proactively fetch images.

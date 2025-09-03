---
layout: default-layout
title: ProactiveImageSourceAdapter Class - Dynamsoft Utility Module .NET Edition API Reference
description: Definition of ProactiveImageSourceAdapter class in Dynamsoft Utility Module .NET Edition.
keywords: proactive image source adapter, .NET
needAutoGenerateSidebar: true
---

# ProactiveImageSourceAdapter

The `ProactiveImageSourceAdapter` class is an abstract class that extends the `ImageSourceAdapter` class. It provides interfaces for proactively fetching images in a separate thread.

## Definition

*Namespace:* Dynamsoft.Utility

*Assembly:* Dynamsoft.Utility.dll

*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-adapter.html) -> ProactiveImageSourceAdapter

```csharp
public class ProactiveImageSourceAdapter : ImageSourceAdapter
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`FetchImage`](#fetchimage) | This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.|
| [`SetImageFetchInterval`](#setimagefetchinterval) | Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`GetImageFetchInterval`](#getimagefetchinterval) | Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`HasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`StartFetching`](#startfetching) | Starts fetching images. |
| [`StopFetching`](#stopfetching) | Stops fetching images. |
| [`Dispose`](#dispose) | Releases all resources used by current object. |

### FetchImage

This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.

```csharp
abstract ImageData FetchImage()
```

**Return Value**

Returns an `ImageData` object representing the fetched image.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SetImageFetchInterval

Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```csharp
void SetImageFetchInterval(int milliseconds)
```

**Parameters**

- `[in] milliseconds` Specifies the wait time in milliseconds. If setting to -1, the `ImageSource` does not proactively fetch images.

### GetImageFetchInterval

Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```csharp
int GetImageFetchInterval()
```

**Return Value**

Returns the wait time in milliseconds. If the value is -1, the `ImageSource` does not proactively fetch images.

### HasNextImageToFetch

Determines whether there are more images left to fetch.

```csharp
override bool HasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

### StartFetching

Starts fetching images.

```csharp
override void StartFetching()
```

### StopFetching

Stops fetching images.

```csharp
override void StopFetching()
```

### Dispose

Releases all resources used by current object.

```csharp
override void Dispose()
```

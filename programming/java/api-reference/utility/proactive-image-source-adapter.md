---
layout: default-layout
title: ProactiveImageSourceAdapter Class - Dynamsoft Utility Module Java Edition API Reference
description: Definition of ProactiveImageSourceAdapter class in Dynamsoft Utility Module Java Edition.
keywords: proactive image source adapter, java
needAutoGenerateSidebar: true
---

# ProactiveImageSourceAdapter

The `ProactiveImageSourceAdapter` class is an abstract class that extends the `ImageSourceAdapter` class. It provides classes for proactively fetching images in a separate thread.

## Definition

*Package:* com.dynamsoft.utility

*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_java_api }}core/basic-classes/image-source-adapter.html) -> ProactiveImageSourceAdapter

```java
public abstract class ProactiveImageSourceAdapter extends ImageSourceAdapter
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`fetchImage`](#fetchimage) | This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.|
| [`setImageFetchInterval`](#setimagefetchinterval) | Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`getImageFetchInterval`](#getimagefetchinterval) | Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`startFetching`](#startfetching) | Starts fetching images. |
| [`stopFetching`](#stopfetching) | Stops fetching images. |

### fetchImage

This method needs to be implemented in the derived class. It is called in a loop in the Fetching thread to obtain images.

```java
protected abstract ImageData fetchImage()
```

**Return Value**

Returns an `ImageData` object representing the fetched image.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setImageFetchInterval

Sets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```java
void setImageFetchInterval(int milliseconds)
```

**Parameters**

`milliseconds` Specifies the wait time in milliseconds. If setting to -1, the `ImageSource` does not proactively fetch images.

### getImageFetchInterval

Gets the time interval for the `ImageSource` to wait before attempting to fetch another image to put in the buffer.

```java
int getImageFetchInterval()
```

**Return Value**

Returns the wait time in milliseconds. If the value is -1, the `ImageSource` does not proactively fetch images.

### hasNextImageToFetch

Determines whether there are more images left to fetch.

```java
boolean hasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

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

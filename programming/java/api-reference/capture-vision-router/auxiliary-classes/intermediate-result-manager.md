---
layout: default-layout
title: class IntermediateResultManager - Dynamsoft Capture Vision Router Java Edition API Reference
description: This page shows the Java Edition of the class IntermediateResultManager in Dynamsoft Capture Vision Router Module.
keywords: intermediate result manager, java
needAutoGenerateSidebar: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Package:* com.dynamsoft.cvr

```java
public final class IntermediateResultManager 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`AddResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`removeResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`getOriginalImage`](#getoriginalimage) | Gets the original image data using an image hash id. |

### AddResultReceiver

Adds an intermediate result receiver to the manager.

```java
public void AddResultReceiver(IntermediateResultReceiver receiver) throws CaptureVisionException
```

**Parameters**

`receiver` The intermediate result receiver to add.

**Return value**

Returns void.

**Exception**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### removeResultReceiver

Removes an intermediate result receiver from the manager.

```java
public void removeResultReceiver(IntermediateResultReceiver receiver) throws CaptureVisionException
```

**Parameters**

`receiver` The intermediate result receiver to remove.

**Return value**

Returns void.

**Exception**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### getOriginalImage

Gets the original image data using an image hash id.

```java
public ImageData getOriginalImage(String imageHashId)
```

**Parameters**

`imageHashId` The hash id of the image to retrieve.

**Return value**

Returns an `ImageData` object containing the original image data.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

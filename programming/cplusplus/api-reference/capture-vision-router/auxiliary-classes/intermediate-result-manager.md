---
layout: default-layout
title: class CIntermediateResultManager - Dynamsoft Capture Vision Router C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultManager in Dynamsoft Capture Vision Router Module.
keywords: intermediate result manager, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultManager

The `CIntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CIntermediateResultManager 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`AddResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`RemoveResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`GetOriginalImage`](#getoriginalimage) | Gets the original image data using an image hash id. |

### AddResultReceiver

Adds an intermediate result receiver to the manager.

```cpp
virtual int AddResultReceiver(CIntermediateResultReceiver* receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to add.

**See Also**

[CIntermediateResultReceiver]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)

### RemoveResultReceiver

Removes an intermediate result receiver from the manager.

```cpp
virtual int RemoveResultReceiver(CIntermediateResultReceiver* receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to remove.

**See Also**

[CIntermediateResultReceiver]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)

### GetOriginalImage

Gets the original image data using an image hash id.

```cpp
virtual CImageData* GetOriginalImage(const char* imageHashId)
```

**Parameters**

`[in] imageHashId` The hash id of the image to retrieve.

**Return value**

Returns a pointer to the `CImageData` object containing the original image data. You don't need to release the memory pointed to by the returned pointer.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

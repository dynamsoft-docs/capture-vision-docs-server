---
layout: default-layout
title: class IntermediateResultManager - Dynamsoft Capture Vision Router .NET Edition API Reference
description: This page shows the .NET Edition of the class IntermediateResultManager in Dynamsoft Capture Vision Router Module.
keywords: intermediate result manager, .NET
needAutoGenerateSidebar: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
class IntermediateResultManager 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`AddResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver.|
| [`RemoveResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`GetOriginalImage`](#getoriginalimage) | Gets the original image data using an image hash id. |

### AddResultReceiver

Adds an intermediate result receiver to the manager.

```csharp
int AddResultReceiver(IntermediateResultReceiver receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to add.

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### RemoveResultReceiver

Removes an intermediate result receiver from the manager.

```csharp
int RemoveResultReceiver(IntermediateResultReceiver receiver)
```

**Parameters**

`[in] receiver` The intermediate result receiver to remove.

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### GetOriginalImage

Gets the original image data using an image hash id.

```csharp
ImageData GetOriginalImage(string imageHashId)
```

**Parameters**

`[in] imageHashId` The hash id of the image to retrieve.

**Return value**

Returns the `ImageData` object containing the original image data.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

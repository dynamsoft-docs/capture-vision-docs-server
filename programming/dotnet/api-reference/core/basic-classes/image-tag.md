---
layout: default-layout
title: ImageTag Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of ImageTag class in Dynamsoft Core Module .NET Edition.
keywords: image tag, .NET
needAutoGenerateSidebar: true
---

# ImageTag

The `ImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public abstract class ImageTag 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetImageTagType`](#getimagetagtype) | Gets the type of the image tag. |
| [`Clone`](#clone) | Creates a copy of the image tag. |
| [`GetImageId`](#getimageid) | Gets the ID of the image. |
| [`SetImageId`](#setimageid) | Sets the ID of the image. |
| [`GetImageCaptureDistanceMode`](#getimagecapturedistancemode) | Gets the capture distance mode of the image. |
| [`SetImageCaptureDistanceMode`](#setimagecapturedistancemode) | Sets the capture distance mode of the image. |

### GetImageTagType

Gets the type of the image tag.

```csharp
abstract EnumImageTagType GetImageTagType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_enumerations }}core/image-tag-type.html?lang=dotnet)

### Clone

Creates a copy of the image tag.

```csharp
abstract ImageTag Clone()
```

**Return Value**

Returns a copy of the image tag.

### GetImageId

Gets the ID of the image.

```csharp
int GetImageId()
```

**Return Value**

Returns the ID of the image.

### SetImageId

Sets the ID of the image.

```csharp
void SetImageId(int imgId)
```

**Parameters**

`[in] imgId` The ID of the image.

### GetImageCaptureDistanceMode

Gets the capture distance mode of the image.

```csharp
EnumImageCaptureDistanceMode GetImageCaptureDistanceMode()
```

**Return Value**

Returns the capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_enumerations }}core/image-capture-distance-mode.html?lang=dotnet)

### SetImageCaptureDistanceMode

Sets the capture distance mode of the image.

```csharp
void SetImageCaptureDistanceMode(EnumImageCaptureDistanceMode mode)
```

**Parameters**

`[in] mode` The capture distance mode of the image.

**See Also**

[EnumImageCaptureDistanceMode]({{ site.dcvb_enumerations }}core/image-capture-distance-mode.html?lang=dotnet)

---
layout: default-layout
title: ImageData Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of ImageData class in Dynamsoft Core Module .NET Edition.
keywords: image data, .NET
needAutoGenerateSidebar: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public class ImageData 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageData()`](#ImageData-constructor4) | Constructs an empty image data object. |
| [`ImageData(byte[] bytes, int width, int height, int stride, EnumImagePixelFormat format, int orientation = 0, ImageTag tag = null)`](#ImageData-constructor) | Constructs an image data object with the specified parameters. |
| [`GetBytes`](#getbytes) | Gets the image byte array. |
| [`GetWidth`](#getwidth) | Gets the width of the image. |
| [`GetHeight`](#getheight) | Gets the height of the image. |
| [`GetStride`](#getstride) | Gets the stride of the image. |
| [`GetImagePixelFormat`](#getimagepixelformat) | Gets the pixel format of the image. |
| [`GetOrientation`](#getorientation) | Gets the orientation of the image. |
| [`GetImageTag`](#getimagetag) | Gets the tag of the image. |
| [`SetImageTag`](#setimagetag) | Sets the tag of the image. |
| [`Dispose`](#dispose) | Releases all resources used by current object. |


### ImageData Constructor

Constructs an image data object with the specified parameters.

```csharp
ImageData(byte[] bytes, int width, int height, int stride, EnumImagePixelFormat format, int orientation = 0, ImageTag tag = null)
```

**Parameters**

`bytes` The image byte array.

`width` The width of the image.

`height` The height of the image.

`stride` The stride of the image.

`format` The pixel format of the image.

`orientation` The orientation of the image.

`tag` The tag of the image.

**See Also**

[EnumImagePixelFormat]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=dotnet)

### GetBytes

Gets the image byte array.

```csharp
byte[] GetBytes()
```

**Return Value**

Returns an image byte array.

### GetWidth

Gets the width of the image.

```csharp
int GetWidth()
```

**Return Value**

Returns the width of the image.

### GetHeight

Gets the height of the image.

```csharp
int GetHeight()
```

**Return Value**

Returns the height of the image.

### GetStride

Gets the stride of the image.

```csharp
int GetStride()
```

**Return Value**

Returns the stride of the image.

### GetImagePixelFormat

Gets the pixel format of the image.

```csharp
EnumImagePixelFormat GetImagePixelFormat()
```

**Return Value**

Returns the pixel format of the image.

**See Also**

[EnumImagePixelFormat]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=dotnet)

### GetOrientation

Gets the orientation of the image.

```csharp
int GetOrientation()
```

**Return Value**

Returns the orientation of the image.

### GetImageTag

Gets the tag of the image.

```csharp
ImageTag GetImageTag()
```

**Return Value**

Returns a tag of the image.

**See Also**

[ImageTag]({{ site.dcv_dotnet_api }}core/basic-classes/image-tag.html)

### SetImageTag

Sets the tag of the image.

```csharp
void SetImageTag(ImageTag tag)
```

**Parameters**

`tag` The tag of the image.

**See Also**

[ImageTag]({{ site.dcv_dotnet_api }}core/basic-classes/image-tag.html)

### Dispose

Releases all resources used by current object.

```csharp
void Dispose()
```


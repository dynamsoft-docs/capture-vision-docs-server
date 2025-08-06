---
layout: default-layout
title: ImageData Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of ImageData class in Dynamsoft Core Module Java Edition.
keywords: image data, java
needAutoGenerateSidebar: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class ImageData
```

## Attributes

| Attribute               | Type | Description |
|-------------------------|------|-------------|
| [`bytesLength`](#byteslength) | *long* | The length of the image byte array. |
| [`bytes`](#bytes) | *byte[]* | The image byte array. |
| [`width`](#width) | *int* | The width of the image. |
| [`height`](#height) | *int* | The height of the image. |
| [`stride`](#stride) | *int* | The stride of the image. |
| [`format`](#format) | *int* | The pixel format of the image. |
| [`orientation`](#orientation) | *int* | The orientation of the image. |
| [`tag`](#tag) | *ImageTag* | The tag of the image. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageData`](#imagedata) | Constructor. Initializes a new instance of the `ImageData` class. |
| [`getBytes`](#getbytes) | Gets the image byte array. |
| [`getBytesLength`](#getbyteslength) | Gets the length of the image byte array. |
| [`getWidth`](#getwidth) | Gets the width of the image. |
| [`getHeight`](#getheight) | Gets the height of the image. |
| [`getStride`](#getstride) | Gets the stride of the image. |
| [`getImagePixelFormat`](#getimagepixelformat) | Gets the pixel format of the image. |
| [`getOrientation`](#getorientation) | Gets the orientation of the image. |
| [`getImageTag`](#getimagetag) | Gets the tag of the image. |
| [`setImageTag`](#setimagetag) | Sets the tag of the image. |

## Attributes

### bytesLength

The length of the image byte array.

```java
long bytesLength
```

### bytes

The image byte array.

```java
byte[] bytes
```

### width

The width of the image.

```java
int width
```

### height

The height of the image.

```java
int height
```

### stride

The stride of the image.

```java
int stride
```

### format

The pixel format of the image.

```java
@EnumImagePixelFormat int format
```

### orientation

The orientation of the image.

```java
int orientation
```

### tag

The tag of the image.

```java
ImageTag tag
```

## Methods

### ImageData

Constructor. Initializes a new instance of the `ImageData` class

```java
ImageData(byte[] bytes, int width, int height, int stride, int format, int orientation, ImageTag tag)
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

[EnumImagePixelFormat]({{ site.dcvb_java_api }}core/enum-image-pixel-format.html)

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### getBytes

Gets the image byte array.

```java
byte[] getBytes()
```

**Return Value**

Returns an image byte array.

### getBytesLength

Gets the length of the image byte array.

```java
long getBytesLength()
```

**Return Value**

Returns the length of the image byte array.

### getWidth

Gets the width of the image.

```java
int getWidth()
```

**Return Value**

Returns the width of the image.

### getHeight

Gets the height of the image.

```java
int getHeight()
```

**Return Value**

Returns the height of the image.

### getStride

Gets the stride of the image.

```java
int getStride()
```

**Return Value**

Returns the stride of the image.

### getImagePixelFormat

Gets the pixel format of the image.

```java
@EnumImagePixelFormat int getImagePixelFormat()
```

**Return Value**

Returns the pixel format of the image.

**See Also**

[EnumImagePixelFormat]({{ site.dcvb_java_api }}core/enum-image-pixel-format.html)

### getOrientation

Gets the orientation of the image.

```java
int getOrientation()
```

**Return Value**

Returns the orientation of the image.

### getImageTag

Gets the tag of the image.

```java
ImageTag getImageTag()
```

**Return Value**

Returns a tag of the image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### setImageTag

Sets the tag of the image.

```java
void setImageTag(ImageTag tag)
```

**Parameters**

`tag` The tag of the image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)


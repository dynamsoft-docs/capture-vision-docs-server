---
layout: default-layout
title: class CImageData - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageData in Dynamsoft Core Module.
keywords: image data, c++
needAutoGenerateSidebar: true
---

# CImageData

The CImageData class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

```cpp
class dynamsoft::core::basic_structures::CImageData 
```

---

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`CImageData()`](#cimagedata-constructor) | Constructs an empty image data object. |
| [`CImageData(int _bytesLength, const unsigned char* _bytes, int _width, int _height, int _stride, ImagePixelFormat _format, int _orientation=0, const CImageTag* _tag = NULL)`](#cimagedata-constructor2) | Constructs an image data object with the specified parameters. |
| [`~CImageData()`](#cimagedata-destructor) | Destructs the image data object and frees the allocated memory. |
| [`GetBytes`](#getbytes) | It is used to get the image byte array. |
| [`GetBytesLength`](#getbyteslength) | It is used to get the length of the image byte array. |
| [`GetWidth`](#getwidth) | It is used to get the width of the image. |
| [`GetHeight`](#getheight) | It is used to get the height of the image. |
| [`GetStride`](#getstride) | It is used to get the stride of the image. |
| [`GetImagePixelFormat`](#getimagepixelformat) | It is used to get the pixel format of the image. |
| [`GetOrientation`](#getorientation) | It is used to get the orientation of the image. |
| [`GetImageTag`](#getimagetag) | It is used to get the tag of the image. |
| [`SetImageTag`](#setimagetag) | It is used to set the tag of the image. |

### CImageData Constructor

Constructs an empty image data object.

```cpp
CImageData()
```

### CImageData Constructor2

Constructs an image data object with the specified parameters.

```cpp
CImageData(int _bytesLength, const unsigned char* _bytes, int _width, int _height, int _stride, ImagePixelFormat _format, int _orientation=0, const CImageTag* _tag = NULL)
```

**Parameters**

`_bytesLength` The length of the image byte array.

`_bytes` The image byte array.

`_width` The width of the image.

`_height` The height of the image.

`_stride` The stride of the image.

`_format` The pixel format of the image.

`_orientation` The orientation of the image.

`_tag` The tag of the image.

### ~CImageData Destructor

Destructs the image data object and frees the allocated memory.

```cpp
virtual ~CImageData()
```

### GetBytes

It is used to get the image byte array.

```cpp
const unsigned char* GetBytes() const
```

**Return value**

Returns a pointer to the image byte array.

### GetBytesLength

It is used to get the length of the image byte array.

```cpp
int GetBytesLength() const
```

**Return value**

Returns the length of the image byte array.

### GetWidth

It is used to get the width of the image.

```cpp
int GetWidth() const
```

**Return value**

Returns the width of the image.

### GetHeight

It is used to get the height of the image.

```cpp
int GetHeight() const
```

**Return value**

Returns the height of the image.

### GetStride

It is used to get the stride of the image.

```cpp
int GetStride() const
```

**Return value**

Returns the stride of the image.

### GetImagePixelFormat

It is used to get the pixel format of the image.

```cpp
ImagePixelFormat GetImagePixelFormat() const
```

**Return value**

Returns the pixel format of the image.

### GetOrientation

It is used to get the orientation of the image.

```cpp
int GetOrientation() const
```

**Return value**

Returns the orientation of the image.

### GetImageTag

It is used to get the tag of the image.

```cpp
const CImageTag* GetImageTag() const
```

**Return value**

Returns a pointer to the tag of the image.

### SetImageTag

It is used to set the tag of the image.

```cpp
void SetImageTag(const CImageTag* _tag)
```

**Parameters**

`_tag` The tag of the image.

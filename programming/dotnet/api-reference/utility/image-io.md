---
layout: default-layout
title: class ImageIO - Dynamsoft Utility Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ImageIO in Dynamsoft Utility Module.
keywords: image io, .NET
needAutoGenerateSidebar: true
---

# ImageIO

The `ImageIO` class handles image reading and writing (from/to files and memory).

## Definition

*Namespace:* Dynamsoft.Utility


```csharp
class ImageIO : IDisposable
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ReadFromBase64String`](#readfrombase64string) | Reads an image from a base64 encoded string. |
| [`ReadFromBitmap`](#readfrombitmap) | Reads an image from a `Bitmap` instance. |
| [`ReadFromFile`](#readfromfile) | Reads an image from a file. |
| [`ReadFromMemory`](#readfrommemory) | Reads an image from a file in memory. |
| [`SaveToBase64String`](#savetobase64string) | Saves an image to a base64 encoded string. |
| [`SaveToBitmap`](#savetobitmap) | Saves an image into a `Bitmap` instance. |
| [`SaveToFile`](#savetofile) | Saves an image to a file. |
| [`SaveToMemory`](#savetomemory) | Saves an image to a file in memory. |

### ReadFromBase64String

Reads an image from a base64 encoded string.

```csharp
ImageData ReadFromBase64String(string base64String, out int errorCode)
```

**Parameters**

`[in] base64String` A base64 encoded string that represents an image.

`[out] errorCode` The error code.

**Return value**

Returns an `ImageData` object representing the image if succeeds, null otherwise.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### ReadFromBitmap

Reads an image from a `Bitmap` instance.

```csharp
ImageData ReadFromBitmap(Bitmap bitmap, out int errorCode)
```

**Parameters**

`[in] bitmap` The source bitmap to read from.

`[out] errorCode` The error code.

**Return value**

Returns an `ImageData` object representing the image if succeeds, null otherwise.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### ReadFromFile

Reads an image from a file.

```csharp
ImageData ReadFromFile(string filePath, out int errorCode)
```

**Parameters**

`[in] filePath` The path of the image file.

`[out] errorCode` The The error code.

**Return value**

Returns an `ImageData` object representing the image if succeeds, null otherwise.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### ReadFromMemory

Reads an image from a file in memory.

```csharp
ImageData ReadFromMemory(byte[] imageFileBytes, out int errorCode)
```

**Parameters**

`[in] imageFileBytes` An array of unsigned char representing the image file in memory.

`[out] errorCode` The The error code.

**Return value**

Returns an `ImageData` object representing the image if succeeds, null otherwise.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SaveToBase64String

Saves an image to a base64 encoded string.

```csharp
int SaveToBase64String(ImageData imageData, EnumImageFileFormat imageFormat, out string base64String)
```

**Parameters**

`[in] imageData` The image data to be saved.

`[in] imageFormat` The image file format to be saved.

`[in] base64String` A base64 encoded string that represents an image.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[ImageFileFormat]({{ site.dcvb_dotnet_api }}core/enum-image-file-format.html)

### SaveToBitmap

Saves an image into a `Bitmap`.

```csharp
int SaveToBitmap(ImageData imageData, out Bitmap bitmap)
```

**Parameters**

`[in] imageData` The image data to be saved.

`[in] bitmap` A `Bitmap` instance that represents an image.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SaveToFile

Saves an image to a file.

```csharp
int SaveToFile(ImageData imageData, string path, bool overwrite = true)
```

**Parameters**

`[in] imageData` The image data to be saved.

`[in] path` The targeting file path with the file name and extension name.

`[in] overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### SaveToMemory

Saves an image to a file in memory.

```csharp
int SaveToMemory(ImageData imageData, EnumImageFileFormat imageFormat, out byte[] imageFileBytes)
```

**Parameters**

`[in] imageData` The image data to be saved.

`[in] imageFormat` The image file format to be saved.

`[out] imageFileBytes` An array of unsigned char representing the image file in memory.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[EnumImageFileFormat]({{ site.dcvb_dotnet_api }}core/enum-image-file-format.html)

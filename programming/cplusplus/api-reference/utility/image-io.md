---
layout: default-layout
title: class CImageIO - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageIO in Dynamsoft Utility Module.
keywords: image io, c++
needAutoGenerateSidebar: true
---

# CImageIO

The `CImageIO` class handles image reading and writing (from/to files and memory).

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CImageIO
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ReadFromFile`](#readfromfile) | Reads an image from a file. |
| [`ReadFromMemory`](#readfrommemory) | Reads an image from a file in memory. |
| [`SaveToFile`](#savetofile) | Saves an image to a file. |
| [`SaveToMemory`](#savetomemory) | Saves an image to a file in memory. |

### ReadFromFile

Reads an image from a file.

```cpp
CImageData* ReadFromFile(const char* filePath, int* pErrorCode = NULL)
```

**Parameters**

`[in] filePath` The path of the image file.

`[out] pErrorCode` The The error code.

**Return value**

Returns a pointer to a `CImageData` object representing the image if succeeds, nullptr otherwise.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file. The caller is responsible for freeing the memory allocated for the image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### ReadFromMemory

Reads an image from a file in memory.

```cpp
CImageData* ReadFromMemory(const unsigned char* imageFileBytes, int imageFileBytesLength, int* pErrorCode = NULL)
```

**Parameters**

`[in] imageFileBytes` An array of unsigned char representing the image file in memory.

`[in] imageFileBytesLength` The length of the image file in bytes.

**Return value**

Returns a pointer to a `CImageData` object representing the image if succeeds, nullptr otherwise.

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file. The caller is responsible for freeing the memory allocated for the image.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SaveToFile

Saves an image to a file.

```cpp
int SaveToFile(const CImageData *pImageData, const char *path, bool overwrite = true)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be saved.

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

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SaveToMemory

Saves an image to a file in memory.

```cpp
int SaveToMemory(const CImageData* pImageData, ImageFileFormat imageFormat, unsigned char** imageFileBytes, int* imageFileBytesLength)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be saved.

`[in] imageFormat` The image file format to be saved.

`[out] imageFileBytes` An array of unsigned char representing the image file in memory.

`[out] imageFileBytesLength` The length of the image file in bytes.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

[ImageFileFormat]({{ site.dcvb_cpp_api }}core/enums/image-file-format.html)

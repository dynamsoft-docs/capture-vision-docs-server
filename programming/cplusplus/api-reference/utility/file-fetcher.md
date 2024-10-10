---
layout: default-layout
title: class CFileFetcher - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CFileFetcher in Dynamsoft Utility Module.
keywords: file fetcher, c++
needAutoGenerateSidebar: true
---

# CFileFetcher

The `CFileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `CImageSourceAdapter` class.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CFileFetcher : public CImageSourceAdapter
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`SetFile`](#setfile) | Sets the file using a file path, file bytes or an `CImageData` object. |
| [`SetPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |
| [`SetPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |

### SetFile

Sets the file using a file path, file bytes or an `CImageData` object.

```cpp
int SetFile(const char* path);
int SetFile(const unsigned char* pFileBytes,int fileSize);
int SetFile(const CImageData* imageData);
```

**Parameters**

`[in] path` The file path.

`[in] pFileBytes`  The file bytes.

`[in] fileSize` The file bytes length.

`[in] imageData` The image data object.

**Return value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

### SetPDFReadingParameter

Sets the parameters for reading PDF files.

```cpp
int SetPDFReadingParameter(const CPDFReadingParameter& para)
```

**Parameters**

`[in] para` The parameter object for reading PDF files.

**Return value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |

**See Also**

[CPDFReadingParameter]({{ site.dcvb_cpp_api }}core/basic-structures/pdf-reading-parameter.html)

### SetPages

Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. By default, there is no restriction on the number of pages that can be decoded in a single file.

```cpp
int SetPages(const int pages[], int pagesCount)
```

**Parameters**

`[in] pages` An integer array containing the page information to be set.

`[in] pagesCount` The number of elements in the array.

**Return value**

Returns an integer value that represents the success or failure of the operation.

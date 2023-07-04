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

### SetFile

Sets the file using a file path, file bytes or an `CImageData` object.

```cpp
int SetFile(const char* path);
int SetFile(const unsigned char* pFileBytes,int fileSize);
int SetFile(const CImageData* imageData);
```

**Parameters**

`[in] path` The file path.

`[in] pFileBytes`  The file bytes..

`[in] fileSize` The file bytes length.

`[in] imageData` The image data object.

**Return value**

Returns an integer value that represents the success or failure of the operation.

### SetPDFReadingParameter

Sets the parameters for reading PDF files.

```cpp
int SetPDFReadingParameter(const CPDFReadingParameter& para)
```

**Parameters**

`[in] para` The parameter object for reading PDF files.

**Return value**

Returns an integer value that represents the success or failure of the operation.

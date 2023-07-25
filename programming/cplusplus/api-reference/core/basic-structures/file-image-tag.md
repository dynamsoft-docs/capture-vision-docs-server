---
layout: default-layout
title: class CFileImageTag - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CFileImageTag in Dynamsoft Core Module.
keywords: file image tag, c++
needAutoGenerateSidebar: true
---

# CFileImageTag

The CFileImageTag class represents an image tag that is associated with a file. It inherits from the CImageTag class and adds additional attributes.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CFileImageTag : public CImageTag
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetFilePath`](#getfilepath) | Gets the file path of the image.|
| [`GetPageNumber`](#getpagenumber) | Gets the page number of the current image in the PDF file. |
| [`GetTotalPages`](#gettotalpages) | Gets the total page number of the PDF file. |
| [`CFileImageTag`](#cfileimagetag-constructor) | The constructor of the CFileImageTag class. |
| [`~CFileImageTag`](#cfileimagetag-destructor) | The destructor of the CFileImageTag class. |

### GetFilePath

Gets the file path of the image tag.

```cpp
const char* GetFilePath() const
```

**Return value**

Returns the file path of the image tag.

### GetPageNumber

Get the page number of the current image in the PDF file.

```cpp
int GetPageNumber() const
```

**Return value**

Returns the page number of the current image in the PDF file.

### GetTotalPages

Gets the total page number of the PDF file.

```cpp
int GetTotalPages() const;
```

**Return value**

Returns the total page number of the PDF file.

### CFileImageTag Constructor

The constructor of the CFileImageTag class.

```cpp
CFileImageTag(const char* _filePath, int _pageNumber)
```

**Parameters**

`[in] _filePath` The file path of the image tag.

`[in] _pageNumber` The page number of the image tag.

### CFileImageTag Destructor

The destructor of the CFileImageTag class. It frees the memory allocated for the file path.

```cpp
virtual ~CFileImageTag()
```

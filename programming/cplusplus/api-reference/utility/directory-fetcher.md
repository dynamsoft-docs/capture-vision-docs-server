---
layout: default-layout
title: class CDirectoryFetcher - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CDirectoryFetcher in Dynamsoft Utility Module.
keywords: directory fetcher, c++
needAutoGenerateSidebar: true
---

# CDirectoryFetcher

The `CDirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `CProactiveImageSourceAdapter` class.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CDirectoryFetcher : public CProactiveImageSourceAdapter
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`SetDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`SetPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |
| [`SetPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |

### SetDirectory

Sets the directory path and filter for the file search.

```cpp
int SetDirectory(const char *path, const char *filter, bool recursive)
```

**Parameters**

`[in] path` The path of the directory to search.

`[in] filter` A string that specifies file extensions. For example: "*.BMP;*.JPG;*.GIF", or "*.*", etc.

`[in] recursive` Specifies whether to load files recursively.

**Return value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

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

[CPDFReadingParameter]({{ site.dcv_cpp_api }}core/basic-structures/pdf-reading-parameter.html)

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

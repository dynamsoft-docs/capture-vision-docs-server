---
layout: default-layout
title: DirectoryFetcher Class - Dynamsoft Utility Module .NET Edition API Reference
description: Definition of DirectoryFetcher class in Dynamsoft Utility Module .NET Edition.
keywords: directory fetcher, .NET
needAutoGenerateSidebar: true
---

# DirectoryFetcher

The `DirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `ProactiveImageSourceAdapter` class.

## Definition

*Namespace:* Dynamsoft.Utility


*Inheritance:* [ProactiveImageSourceAdapter]({{ site.dcvb_dotnet_api }}utility/proactive-image-source-adapter.html) -> DirectoryFetcher

```csharp
public class DirectoryFetcher : ProactiveImageSourceAdapter
```

## Methods

| Method | Description |
|--------|-------------|
| [`DirectoryFetcher`](#directoryfetcher) | Default constructor and destructor of a `DirectoryFetcher` object. |
| [`SetDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`SetPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |
| [`SetPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| [`HasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |

### DirectoryFetcher

Default constructor and destructor of a `DirectoryFetcher` object.

```csharp
DirectoryFetcher()
~DirectoryFetcher()
```

### SetDirectory

Sets the directory path and filter for the file search.

```csharp
int SetDirectory(string path, string filter = "*.bmp;*.jpg;*.jpeg;*.tif;*.png;*.tiff;*.gif;*.pdf", bool recursive = false)
```

**Parameters**

`[in] path` The path of the directory to search.

`[in] filter` A string that specifies file extensions. For example: "\*.BMP;\*.JPG;\*.GIF", or "\*.\*", etc.

`[in] recursive` Specifies whether to load files recursively.

**Return Value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

### SetPDFReadingParameter

Sets the parameters for reading PDF files.

```csharp
int SetPDFReadingParameter(PDFReadingParameter para)
```

**Parameters**

`[in] para` The parameter object for reading PDF files.

**Return Value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |

**See Also**

[PDFReadingParameter]({{ site.dcvb_dotnet_api }}core/basic-classes/pdf-reading-parameter.html)

### SetPages

Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. By default, there is no restriction on the number of pages that can be decoded in a single file.

```csharp
int SetPages(int[] pages)
```

**Parameters**

`[in] pages` An integer array containing the page information to be set.

**Return Value**

Returns an integer value that represents the success or failure of the operation.

### HasNextImageToFetch

Determines whether there are more images left to fetch.

```csharp
override bool HasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

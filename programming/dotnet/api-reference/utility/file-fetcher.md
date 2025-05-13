---
layout: default-layout
title: FileFetcher Class - Dynamsoft Utility Module .NET Edition API Reference
description: Definition of FileFetcher class in Dynamsoft Utility Module .NET Edition.
keywords: file fetcher, .NET
needAutoGenerateSidebar: true
---

# FileFetcher

The `FileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `ImageSourceAdapter` class.

## Definition

*Namespace:* Dynamsoft.Utility


*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-adapter.html) -> FileFetcher

```csharp
public class FileFetcher : ImageSourceAdapter
```

## Methods

| Method | Description |
|--------|-------------|
| [`FileFetcher`](#filefetcher) | Default constructor and destructor of a `FileFetcher` object. |
| [`SetFile`](#setfile) | Sets the file using a file path, file bytes or an `ImageData` object. |
| [`SetPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |
| [`SetPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| [`HasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |

### FileFetcher

Default constructor and destructor of a `FileFetcher` object.

```csharp
FileFetcher()
FileFetcher(PDFReadingParameter pdfReadingParameter)
~FileFetcher()
```

### SetFile

Sets the file using a file path, file bytes or an `ImageData` object.

```csharp
int SetFile(string path);
int SetFile(byte[] bytes);
int SetFile(ImageData imageData);
```

**Parameters**

`[in] path` The file path.

`[in] bytes`  The file bytes.

`[in] imageData` The image data object.

**Return Value**

Returns an integer value that represents the success or failure of the operation.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

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

---
layout: default-layout
title: FileFetcher Class - Dynamsoft Utility Module Java Edition API Reference
description: Definition of FileFetcher class in Dynamsoft Utility Module Java Edition.
keywords: file fetcher, java
needAutoGenerateSidebar: true
---

# FileFetcher

The `FileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `ImageSourceAdapter` class.

## Definition

*Package:* com.dynamsoft.utility

*Inheritance:* [ImageSourceAdapter]({{ site.dcvb_java_api }}core/basic-classes/image-source-adapter.html) -> FileFetcher

```java
public class FileFetcher extends ImageSourceAdapter
```

## Methods

| Method | Description |
|--------|-------------|
| [`FileFetcher`](#filefetcher) | Initializes a new instance of the `FileFetcher` class. |
| [`setFile`](#setfile) | Sets the file using a file path, file bytes or an `ImageData` object. |
| [`setPDFReadingParameter`](#setpdfreadeingparameter) | Sets the parameters for reading PDF files. |
| [`setPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |

### FileFetcher

Initializes a new instance of the `FileFetcher` class.

```java
FileFetcher()
FileFetcher(PDFReadingParameter pdfReadingParameter)
```

**Parameters**

`pdfReadingParameter` A `PDFReadingParameter` object with PDF files reading parameters.

**See Also**

[PDFReadingParameter]({{ site.dcvb_java_api }}core/basic-classes/pdf-reading-parameter.html)

### setFile

Sets the file using a file path, file bytes or an `ImageData` object.

```java
void setFile(String path) throws UtilityException
void setFile(byte[] bytes) throws UtilityException
void setFile(ImageData imageData) throws UtilityException
```

**Parameters**

`path` Specifies the path of the file to process.

`bytes` Specifies the image file bytes in memory to process.

`imageData` Specifies the image data to process.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### setPDFReadingParameter

Sets the parameters for reading PDF files.

```java
void setPDFReadingParameter(PDFReadingParameter para) throws UtilityException
```

**Parameters**

`para` A `PDFReadingParameter` object with PDF files reading parameters.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[PDFReadingParameter]({{ site.dcvb_java_api }}core/basic-classes/pdf-reading-parameter.html)

### setPages

Sets the 0-based page indexes of a file (.tiff or .pdf). By default, there is no restriction on the number of pages that can be processed in a single file.

```java
void setPages(int[] pages) throws UtilityException
```

**Parameters**

`pages` An integer array containing the page information to be set.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

### hasNextImageToFetch

Determines whether there are more images left to fetch.

```java
boolean hasNextImageToFetch()
```

**Return Value**

Returns true if there are more images left to fetch, false otherwise.

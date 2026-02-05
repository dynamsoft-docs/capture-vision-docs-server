---
layout: default-layout
title: DirectoryFetcher Class - Dynamsoft Utility Module Java Edition API Reference
description: Definition of DirectoryFetcher class in Dynamsoft Utility Module Java Edition.
keywords: directory fetcher, java
needAutoGenerateSidebar: true
---

# DirectoryFetcher

The `DirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `ProactiveImageSourceAdapter` class.

## Definition

*Package:* com.dynamsoft.utility

*Inheritance:* [ProactiveImageSourceAdapter]({{ site.dcvb_java_api }}utility/proactive-image-source-adapter.html) -> DirectoryFetcher

```java
public class DirectoryFetcher extends ProactiveImageSourceAdapter
```

## Methods

| Method | Description |
|--------|-------------|
| [`DirectoryFetcher`](#directoryfetcher) | Initializes a new instance of the `DirectoryFetcher` class. |
| [`setDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`setPDFReadingParameter`](#setpdfreadeingparameter) | Sets the parameters for reading PDF files. |
| [`setPages`](#setpages) | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |

### DirectoryFetcher

Initializes a new instance of the `DirectoryFetcher` class.

```java
DirectoryFetcher()
```

### setDirectory

Sets the directory path and filter for the file search.

```java
void setDirectory(String filePath) throws UtilityException
void setDirectory(String filePath, String filter, boolean recursive) throws UtilityException
```

**Parameters**

`filePath` The path of the directory to search.

`filter` A string that specifies file extensions. For example: "*.BMP;*.JPG;*.GIF", or "*.*", etc. The default value is "*.bmp;*.jpg;*.jpeg;*.tif;*.png;*.tiff;*.gif;*.pdf".

`recursive` Specifies whether to load files recursively. The default value is false.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

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


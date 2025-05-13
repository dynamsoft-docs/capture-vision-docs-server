---
layout: default-layout
title: FileImageTag Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of FileImageTag class in Dynamsoft Core Module .NET Edition.
keywords: file image tag, .NET
needAutoGenerateSidebar: true
---

# FileImageTag

The `FileImageTag` class represents an image tag that is associated with a file. It inherits from the `ImageTag` class and adds additional attributes.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
public class FileImageTag : ImageTag
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`FileImageTag`](#FileImageTag-constructor) | The constructor of the FileImageTag class. |
| [`GetFilePath`](#getfilepath) | Gets the file path of the image.|
| [`GetPageNumber`](#getpagenumber) | Gets the page number of the current image in the Multi-Page image file. |
| [`GetTotalPages`](#gettotalpages) | Gets the total page number of the Multi-Page image file. |
| [`GetImageTagType`](#getimagetagtype) | Gets the type of the image tag. |
| [`Clone`](#clone) | Creates a copy of the image tag. |

### FileImageTag Constructor

The constructor of the `FileImageTag` class.

```csharp
FileImageTag(string filePath, int pageNumber, int totalPages)
```

**Parameters**

`[in] filePath` The file path of the image tag.

`[in] pageNumber` The page number of the current image in the Multi-Page image file.

`[in] totalPages` The total page number of the Multi-Page image file.

### GetFilePath

Gets the file path of the image tag.

```csharp
string GetFilePath()
```

**Return Value**

Returns the file path of the image tag.

### GetPageNumber

Get the page number of the current image in the Multi-Page image file.

```csharp
int GetPageNumber()
```

**Return Value**

Returns the page number of the current image in the Multi-Page image file.

### GetTotalPages

Gets the total page number of the Multi-Page image file.

```csharp
int GetTotalPages()
```

**Return Value**

Returns the total page number of the Multi-Page image file.

### GetImageTagType

Gets the type of the image tag.

```csharp
EnumImageTagType GetImageTagType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_dotnet_api }}core/enum-image-tag-type.html)

### Clone

Creates a copy of the image tag.

```csharp
ImageTag Clone()
```

**Return Value**

Returns a copy of the image tag.

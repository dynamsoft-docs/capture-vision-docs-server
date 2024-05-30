---
layout: default-layout
title: ImageManager Class - Dynamsoft Utility Module .NET Edition API Reference
description: Definition of ImageManager class in Dynamsoft Utility Module .NET Edition.
keywords: image manager, drawing on image, .NET
needAutoGenerateSidebar: true
---

# ImageManager

The `ImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Namespace:* Dynamsoft.Utility

*Assembly:* Dynamsoft.Utility.dll

```csharp
public class ImageManager
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`SaveToFile`](#savetofile) | Saves an image to a file. |

### SaveToFile

Saves an image to a file.

```csharp
int SaveToFile(ImageData imageData, string path, bool overwrite = true)
```

**Parameters**

`[in] imageData` The image data to be saved.

`[in] path` The targeting file path with the file name and extension name.

`[in] overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Return Value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[ImageData]({{ site.dcv_dotnet_api }}core/basic-classes/image-data.html)


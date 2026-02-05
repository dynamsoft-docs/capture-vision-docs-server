---
layout: default-layout
title: class ImageIO - Dynamsoft Utility Module Java Edition API Reference
description: This page shows the Java Edition of the class ImageIO in Dynamsoft Utility Module.
keywords: image io, java
needAutoGenerateSidebar: true
---

# ImageIO

The `ImageIO` class handles image reading and writing (from/to files and memory).

## Definition

*Package:* com.dynamsoft.utility

```java
public class ImageIO
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageIO`](#imageio) | Initializes a new instance of the `ImageIO` class. |
| [`readFromFile`](#readfromfile) | Reads an image from a file. |
| [`readFromMemory`](#readfrommemory) | Reads an image from a file in memory. |
| [`readFromBase64String`](#readfrombase64string) | Reads an image from a Base64 string. |
| [`saveToFile`](#savetofile) | Saves an image to a file. |
| [`saveToMemory`](#savetomemory) | Saves an image to a file in memory. |
| [`saveToBase64String`](#savetobase64string) | Saves an image to a Base64 string. |

### ImageIO

Initializes a new instance of the `ImageIO` class.

```java
ImageIO()
```

### readFromFile

Reads an image from a file.

```java
ImageData readFromFile(String filePath) throws UtilityException
```

**Parameters**

`filePath` The path of the image file.

**Return value**

Returns an `ImageData` object representing the image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### readFromMemory

Reads an image from a file in memory.

```java
ImageData readFromMemory(byte[] fileBytes) throws UtilityException
```

**Parameters**

`fileBytes` A byte array representing the image file in memory.

**Return value**

Returns an `ImageData` object representing the image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**Remarks**

If the file format is gif, pdf or tiff, we read the first page of the image file.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### readFromBase64String

Reads an image from a Base64 string.

```java
ImageData readFromBase64String(String base64String) throws UtilityException
```

**Parameters**

`base64String` A Base64 encoded string representing the image.

**Return value**

Returns an `ImageData` object representing the image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### saveToFile

Saves an image to a file.

```java
void saveToFile(ImageData imageData, String path) throws UtilityException
void saveToFile(ImageData imageData, String path, boolean overwrite) throws UtilityException
```

**Parameters**

`imageData` The image data to be saved.

`path` The targeting file path with the file name and extension name.

`overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### saveToMemory

Saves an image to a file in memory.

```java
byte[] saveToMemory(ImageData imageData, @EnumImageFileFormat int imageFormat) throws UtilityException
```

**Parameters**

`imageData` The image data to be saved.

`imageFormat` The image file format to be saved.

**Return value**

Returns the byte array representing the saved image file.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[EnumImageFileFormat]({{ site.dcvb_java_api }}core/enum-image-file-format.html)

### saveToBase64String

Saves an image to a Base64 string.

```java
String saveToBase64String(ImageData imageData, @EnumImageFileFormat int imageFormat) throws UtilityException
```

**Parameters**

`imageData` The image data to be saved.

`imageFormat` The image file format to be saved.

**Return value**

Returns a Base64 encoded string representing the saved image.

**Exception**

[UtilityException]({{ site.dcvb_java_api }}utility/utility-exception.html)

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[EnumImageFileFormat]({{ site.dcvb_java_api }}core/enum-image-file-format.html)

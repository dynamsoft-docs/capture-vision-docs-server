---
layout: default-layout
title: FileImageTag Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of FileImageTag class in Dynamsoft Core Module Java Edition.
keywords: file image tag, java
needAutoGenerateSidebar: true
---

# FileImageTag

The `FileImageTag` class represents an image tag that is associated with a file. It inherits from the `ImageTag` class and adds additional attributes.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class FileImageTag extends ImageTag
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`FileImageTag`](#fileimagetag) | Initializes a new instance of the `FileImageTag` class. |
| [`getFilePath`](#getfilepath) | Gets the file path of the image. |
| [`getPageNumber`](#getpagenumber) | Gets the page number of the current image in the Multi-Page image file. |
| [`getTotalPages`](#gettotalpages) | Gets the total page number of the Multi-Page image file. |
| [`getType`](#gettype) | Gets the type of the image tag. |
| [`clone`](#clone) | Creates a copy of the image tag. |

### FileImageTag

Initializes a new instance of the `FileImageTag` class.

```java
public FileImageTag(String filePath, int pageNumber, int totalPages)
```

**Parameters**

`filePath`: The file path of the image tag.

`pageNumber`: The page number of the current image in the Multi-Page image file.

`totalPages`: The total page number of the Multi-Page image file.

### getFilePath

Gets the file path of the image.

```java
public String getFilePath()
```

**Return Value**

Returns the file path of the image tag.

### getPageNumber

Gets the page number of the current image in the Multi-Page image file.

```java
public int getPageNumber()
```

**Return Value**

Returns the page number of the current image in the Multi-Page image file.

### getTotalPages

Gets the total page number of the Multi-Page image file.

```java
public int getTotalPages()
```

**Return Value**

Returns the total page number of the Multi-Page image file.

### getType

Gets the type of the image tag.

```java
public @EnumImageTagType int getType()
```

**Return Value**

Returns the type of the image tag.

**See Also**

[EnumImageTagType]({{ site.dcvb_java_api }}core/enum-image-tag-type.html)

### clone

Creates a copy of the image tag.

```java
public ImageTag clone()
```

**Return Value**

Returns a copy of the `FileImageTag` object.

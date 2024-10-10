---
layout: default-layout
title: OriginalImageResultItem Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of OriginalImageResultItem class in Dynamsoft Core Module .NET Edition.
keywords: original image, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` class represents a captured original image result item. It is a derived class of `CapturedResultItem` and provides an interface to get the image data.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public class OriginalImageResultItem : CapturedResultItem
```

## Methods

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`GetImageData`](#getimagedata) | Gets the image data for the `OriginalImageResultItem`. |
| [`GetCapturedResultItemType`](#getcapturedresultitemtype) | Gets the type of the captured result item. |
| [`GetReferenceItem`](#getreferenceitem) | Gets the referenced item in the captured result item. |

### GetImageData

Gets the image data for the `OriginalImageResultItem`.

```csharp
ImageData GetImageData()
```

**Return Value**

Returns the `ImageData` object that contains the image data for the `OriginalImageResultItem`.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### GetCapturedResultItemType

Gets the type of the captured result item.

```csharp
EnumCapturedResultItemType GetCapturedResultItemType()
```

**Return Value**

Returns the type of the captured result item.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### GetReferenceItem

Gets the referenced item in the captured result item.

```csharp
CapturedResultItem GetReferenceItem()
```

**Return Value**

Returns the referenced item in the captured result item.

**See Also**

[CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html)

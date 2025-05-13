---
layout: default-layout
title: SimplifiedCaptureVisionSettings Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of SimplifiedCaptureVisionSettings class in Dynamsoft Capture Vision Module .NET Edition.
keywords: class, .NET, SimplifiedCaptureVisionSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` class contains settings for capturing and recognizing images with the `CaptureVisionRouter` class.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public class SimplifiedCaptureVisionSettings
```

## Attributes

| Attribute                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [`outputOriginalImage`](#outputOriginalImage) | *int*                               |
| [`roi`](#roi)                                         | *Quadrilateral*                    |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *int*                               |
| [`maxParallelTasks`](#maxparalleltasks)               | *int*                               |
| [`timeout`](#timeout)                                 | *int*                               |
| [`barcodeSettings`](#barcodesettings)                 | *SimplifiedBarcodeReaderSettings*   |
| [`labelSettings`](#labelsettings)                     | *SimplifiedLabelRecognizerSettings* |
| [`documentSettings`](#documentsettings)               | *SimplifiedDocumentNormalizerSettings* |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int*                               |

### outputOriginalImage

Specifies whether to output the original image. 

```csharp
int outputOriginalImage;
```

**Values**

- 0: Do not output the original image.
- 1: Output the original image.


### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place. 

```csharp
Quadrilateral roi;
```

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### roiMeasuredInPercentage

Specifies whether the ROI is measured in pixels or as a percentage of the image size.

```csharp
int roiMeasuredInPercentage;
```

**Values**

- `0` the ROI is measured in pixels.
- `1` the ROI is measured as a percentage of the image size.

### maxParallelTasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

```csharp
int maxParallelTasks;
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```csharp
int timeout;
```

### barcodeSettings

Specifies the settings for barcode recognition.

```csharp
SimplifiedBarcodeReaderSettings barcodeSettings;
```

**See Also**

[SimplifiedBarcodeReaderSettings]({{ site.dbr_dotnet_api }}simplified-barcode-reader-settings.html)

### labelSettings

Specifies the settings for label recognition.

```csharp
SimplifiedLabelRecognizerSettings labelSettings;
```

**See Also**

[SimplifiedLabelRecognizerSettings]({{ site.dlr_dotnet_api }}simplified-label-recognizer-settings.html)

### documentSettings

Specifies the settings for document normalization.

```csharp
SimplifiedDocumentNormalizerSettings documentSettings;
```

**See Also**

[SimplifiedDocumentNormalizerSettings]({{ site.ddn_dotnet_api }}simplified-document-normalizer-settings.html)

### minImageCaptureInterval

Specifies the minimum time interval (in milliseconds) allowed between consecutive image captures.

```csharp
int minImageCaptureInterval;
```

**Remarks**

This property represents the minimum time interval (in milliseconds) that must elapse before the next image capture operation can be initiated.
Setting a larger value for this property will introduce a delay between image captures, while setting a smaller value allows for more frequent captures. It can be used to reduce the computational frequency, which can effectively lower energy consumption. Please note that the actual time interval between captures may be longer than the specified minimum interval due to various factors, such as image processing time and hardware limitations.


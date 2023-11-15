---
layout: default-layout
title: struct SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedCaptureVisionSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedCaptureVisionSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedCaptureVisionSettings Struct
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` struct contains settings for capturing and recognizing images with the `CCaptureVisionRouter` class.

## Definition

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
typedef struct tagSimplifiedCaptureVisionSettings
{
    int capturedResultItemTypes;
    CQuadrilateral roi;
    int roiMeasuredInPercentage;
    int maxParallelTasks;
    int timeout;
    SimplifiedBarcodeReaderSettings barcodeSettings;
    SimplifiedLabelRecognizerSettings labelSettings;
    int minImageCaptureInterval;
    char reserved[2044];
} SimplifiedCaptureVisionSettings;
```

## Attributes Summary

| Attribute                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [`capturedResultItemTypes`](#capturedresultitemtypes) | *int*                               |
| [`roi`](#roi)                                         | *CQuadrilateral*                    |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *int*                               |
| [`maxParallelTasks`](#maxparalleltasks)               | *int*                               |
| [`timeout`](#timeout)                                 | *int*                               |
| [`barcodeSettings`](#barcodesettings)                 | *SimplifiedBarcodeReaderSettings*   |
| [`labelSettings`](#labelsettings)                     | *SimplifiedLabelRecognizerSettings* |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int*                               |
| [`reserved`](#reserved)                               | *char[2044]*                        |

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be captured. 

```cpp
int capturedResultItemTypes
```

**Values**

The value should be a bitwise OR combination of one or more of enumeration `CapturedResultItemType`:

**See Also**

[CapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place. 

```cpp
CQuadrilateral roi
```

**See Also**

[CQuadrilateral]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)

### roiMeasuredInPercentage

Specifies whether the ROI is measured in pixels or as a percentage of the image size.

```cpp
int roiMeasuredInPercentage
```

**Values**

- `0` if the ROI is measured in pixels.
- `1` if the ROI is measured as a percentage of the image size.

### maxParallelTasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

```cpp
int maxParallelTasks
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```cpp
int timeout
```

### barcodeSettings

Specifies the settings for barcode recognition.

```cpp
SimplifiedBarcodeReaderSettings barcodeSettings
```

**See Also**

[SimplifiedBarcodeReaderSettings]({{ site.dbr_cpp_api }}simplified-barcode-reader-settings.html)

### labelSettings

Specifies the settings for label recognition.

```cpp
SimplifiedLabelRecognizerSettings labelSettings
```

**See Also**

[SimplifiedLabelRecognizerSettings]({{ site.dlr_cpp_api }}simplified-label-recognizer-settings.html)

### minImageCaptureInterval

Specifies the minimum time interval (in milliseconds) allowed between consecutive image captures.

```cpp
int minImageCaptureInterval
```

**Remarks**

This property represents the minimum time interval (in milliseconds) that must elapse before the next image capture operation can be initiated.
Setting a larger value for this property will introduce a delay between image captures, while setting a smaller value allows for more frequent captures. It can be used to reduce the computational frequency, which can effectively lower energy consumption. Please note that the actual time interval between captures may be longer than the specified minimum interval due to various factors, such as image processing time and hardware limitations.

### reserved

Reserved for future use.

```cpp
char reserved[2044]
```

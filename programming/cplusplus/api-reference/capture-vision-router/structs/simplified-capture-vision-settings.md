---
layout: default-layout
title: struct SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedCaptureVisionSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedCaptureVisionSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedCaptureVisionSettings Struct
permalink: /programming/cplusplus/api-reference/capture-vision-router/structs/simplified-capture-vision-settings.html
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` struct contains settings for capturing and recognizing images with the `CCaptureVisionRouter` class.

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
    char reserved[2048];
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
| `reserved`                                            | *char[2048]*                        |

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be captured. 

```cpp
int capturedResultItemTypes
```

**Values**

The value should be a bitwise OR combination of one or more of the following constants:
- `DCV_CAPTURED_ITEM_TYPE_BARCODE`
- `DCV_CAPTURED_ITEM_TYPE_LABEL`

### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place. 

```cpp
CQuadrilateral roi
```

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

### labelSettings

Specifies the settings for label recognition.

```cpp
SimplifiedLabelRecognizerSettings labelSettings
```

### reserved

Reserved for future use.

```cpp
char reserved[2048]
```
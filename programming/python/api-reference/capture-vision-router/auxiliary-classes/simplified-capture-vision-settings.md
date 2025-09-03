---
layout: default-layout
title: SimplifiedCaptureVisionSettings Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of SimplifiedCaptureVisionSettings class in Dynamsoft Capture Vision Module Python Edition.
keywords: class, python, SimplifiedCaptureVisionSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` class contains settings for capturing and recognizing images with the `CaptureVisionRouter` class.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class SimplifiedCaptureVisionSettings
```

## Properties

| Attribute                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [`captured_result_item_types`](#captured_result_item_types) | *int*                               |
| [`roi`](#roi)                                         | *Quadrilateral*                    |
| [`roi_measured_in_percentage`](#roi_measured_in_percentage) | *int*                               |
| [`max_parallel_tasks`](#max_parallel_tasks)               | *int*                               |
| [`timeout`](#timeout)                                 | *int*                               |
| [`barcode_settings`](#barcode_settings)                 | *SimplifiedBarcodeReaderSettings*   |
| [`label_settings`](#label_settings)                     | *SimplifiedLabelRecognizerSettings* |
| [`document_settings`](#document_settings)               | *SimplifiedDocumentNormalizerSettings* |
| [`min_image_capture_interval`](#min_image_capture_interval) | *int*                               |

### captured_result_item_types

Specifies the type(s) of captured result item(s) that will be captured. 

**Values**

It is a bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place. 

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### roi_measured_in_percentage

Specifies whether the ROI is measured in pixels or as a percentage of the image size.

**Values**

- `0` the ROI is measured in pixels.
- `1` the ROI is measured as a percentage of the image size.

### max_parallel_tasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

### barcode_settings

Specifies the settings for barcode recognition.

**See Also**

[SimplifiedBarcodeReaderSettings]({{ site.dbr_python_api }}simplified-barcode-reader-settings.html)

### label_settings

Specifies the settings for label recognition.

**See Also**

[SimplifiedLabelRecognizerSettings]({{ site.dlr_python_api }}simplified-label-recognizer-settings.html)

### document_settings

Specifies the settings for document normalization.

**See Also**

[SimplifiedDocumentNormalizerSettings]({{ site.ddn_python_api }}simplified-document-normalizer-settings.html)

### min_image_capture_interval

Specifies the minimum time interval (in milliseconds) allowed between consecutive image captures.

**Remarks**

This property represents the minimum time interval (in milliseconds) that must elapse before the next image capture operation can be initiated.
Setting a larger value for this property will introduce a delay between image captures, while setting a smaller value allows for more frequent captures. It can be used to reduce the computational frequency, which can effectively lower energy consumption. Please note that the actual time interval between captures may be longer than the specified minimum interval due to various factors, such as image processing time and hardware limitations.

## Methods
  
| Method | Description |
|------- | ---- |
| [`__init__`](#__init__) | Initializes a new instance of the `SimplifiedCaptureVisionSettings` class. |

### \_\_init\_\_

Initializes a new instance of the `SimplifiedCaptureVisionSettings` class.

```python
def __init__(self):
```


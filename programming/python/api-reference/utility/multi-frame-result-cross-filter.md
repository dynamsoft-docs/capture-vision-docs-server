---
layout: default-layout
title: MultiFrameResultCrossFilter Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of MultiFrameResultCrossFilter class in Dynamsoft Utility Module Python Edition.
keywords: multiple frame result cross filter, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class is responsible for filtering captured results. As a default implementation of `CapturedResultFilter`, it provides results verification and duplicate results filtering features.

## Definition

*Module:* dynamsoft_utility

*Inheritance:* [CapturedResultFilter]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) -> MultiFrameResultCrossFilter

```python
class MultiFrameResultCrossFilter(dynamsoft_capture_vision_router.CapturedResultFilter)
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`__init__`](#__init__) | Initializes a new instance of the `MultiFrameResultCrossFilter` class. |
| [`enable_result_cross_verification`](#enable_result_cross_verification) | Enable result cross verification feature to improve the accuracy of video streaming recognition results. |
| [`is_result_cross_verification_enabled`](#is_result_cross_verification_enabled) | Determines whether the result cross verification feature is enabled for the specific captured result item type. |
| [`enable_result_deduplication`](#enable_result_deduplication) | Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition. |
| [`is_result_deduplication_enabled`](#is_result_deduplication_enabled) | Determines whether the result deduplication feature is enabled for the specific result item type. |
| [`set_duplicate_forget_time`](#set_duplicate_forget_time) | Sets the duplicate forget time for the specific captured result item types. |
| [`get_duplicate_forget_time`](#get_duplicate_forget_time) | Gets the duplicate forget time for a specific captured result item type. |
| [`set_max_overlapping_frames`](#set_max_overlapping_frames) | Sets the max referencing frames count for the to-the-latest overlapping feature. |
| [`get_max_overlapping_frames`](#get_max_overlapping_frames) | Gets the max referencing frames count for the to-the-latest overlapping feature. |
| [`enable_latest_overlapping`](#enable_latest_overlapping) | Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous. |
| [`is_latest_overlapping_enabled`](#is_latest_overlapping_enabled) | Determines whether the to-the-latest overlapping feature is enabled for the specific result item type. |

### \_\_init\_\_

Initializes a new instance of the `MultiFrameResultCrossFilter` class.

```python
def __init__(self):
```

### enable_result_cross_verification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```python
def enable_result_cross_verification(self, result_item_types: int, enabled: bool) -> None:
```

**Parameters**

`result_item_types` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`enabled` Set whether to enable result verification.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### is_result_cross_verification_enabled

Determines whether the result cross verification feature is enabled for the specific captured result item type.

```python
def is_result_cross_verification_enabled(self, type: int) -> bool:
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a bool value indicating whether result verification is enabled for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### enable_result_deduplication

Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.

```python
def enable_result_deduplication(self, result_item_types: int, enabled: bool) -> None:
```

**Parameters**

`result_item_types` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`enabled` Set whether to enable result result deduplication.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### is_result_deduplication_enabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```python
def is_result_deduplication_enabled(self, type: int) -> bool:
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a bool value indicating whether result deduplication is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### set_duplicate_forget_time

Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period if deduplication feature is enabled. The default value is 3000ms.

```python
def set_duplicate_forget_time(self, result_item_types: int, time: int) -> None:
```

**Parameters**

`result_item_types` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`time` The duplicate forget time measured in milliseconds. The value rang is [1, 180000].

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### get_duplicate_forget_time

Gets the duplicate forget time for a specific captured result item type.

```python
def get_duplicate_forget_time(self, type: int) -> int:
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns the duplicate forget time for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### set_max_overlapping_frames

Sets the max referencing frames count for the to-the-latest overlapping feature.

```python
def set_max_overlapping_frames(self, result_item_types: int, max_overlapping_frames: int) -> None:
```

**Parameters**

`[in] result_item_types` The or value of the captured result item types.

`[in] max_overlapping_frames` The max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### get_max_overlapping_frames

Gets the max referencing frames count for the to-the-latest overlapping feature.

```python
def get_max_overlapping_frames(self, type: int) -> int:
```

**Parameters**

`[in] type` Specifies a specific result item type, which can be defined using `EnumCapturedResultItemType`.

**Return value**

Returns the max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)


### enable_latest_overlapping

Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.

```python
def enable_latest_overlapping(self, result_item_types: int, enabled: bool) -> None:
```

**Parameters**

`[in] result_item_types` The or value of the captured result item types.  
`[in] enabled` Sets whether to enable the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### is_latest_overlapping_enabled

Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.

```python
def is_latest_overlapping_enabled(self, type: int) -> bool:
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether the to-the-latest overlapping feature is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)


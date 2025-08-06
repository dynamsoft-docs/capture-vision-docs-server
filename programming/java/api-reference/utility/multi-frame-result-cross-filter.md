---
layout: default-layout
title: MultiFrameResultCrossFilter Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of MultiFrameResultCrossFilter class in Dynamsoft Utility Module Java Edition.
keywords: multiple frame result cross filter, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class is responsible for filtering captured results. As a default implementation of `CapturedResultFilter`, it provides results verification and duplicate results filtering features.

## Definition

*Namespace:* com.dynamsoft.utility

*Inheritance:* [CapturedResultFilter]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) -> MultiFrameResultCrossFilter

```java
public final class MultiFrameResultCrossFilter extends CapturedResultFilter
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`MultiFrameResultCrossFilter`](#multiframeresultcrossfilter) | Initializes a new instance of the `MultiFrameResultCrossFilter` class. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enable result cross verification feature to improve the accuracy of video streaming recognition results. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Determines whether the result cross verification feature is enabled for the specific captured result item type. |
| [`enableResultDeduplication`](#enableresultdeduplication) | Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Determines whether the result deduplication feature is enabled for the specific result item type. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the duplicate forget time for the specific captured result item types. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the duplicate forget time for a specific captured result item type. |
| [`setMaxOverlappingFrames`](#setmaxoverlappingframes) | Sets the max referencing frames count for the to-the-latest overlapping feature. |
| [`getMaxOverlappingFrames`](#getmaxoverlappingframes) | Gets the max referencing frames count for the to-the-latest overlapping feature. |
| [`enableLatestOverlapping`](#enablelatestoverlapping) | Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous. |

### MultiFrameResultCrossFilter

Initializes a new instance of the `MultiFrameResultCrossFilter` class.

```java
MultiFrameResultCrossFilter()
MultiFrameResultCrossFilter(CaptureVisionRouter router)
```

**Parameters**

`router` A `CaptureVisionRouter` object.

**See Also**

[CaptureVisionRouter]({{ site.dcvb_java_api }}capture-vision-router/capture-vision-router.html)

### enableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```java
void enableResultCrossVerification(int resultItemTypes, boolean enabled)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`enabled` Set whether to enable result verification.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### isResultCrossVerificationEnabled

Determines whether the result cross verification feature is enabled for the specific captured result item type.

```java
boolean isResultCrossVerificationEnabled(@EnumCapturedResultItemType int type)
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a boolean value indicating whether result verification is enabled for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### enableResultDeduplication

Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.

```java
void enableResultDeduplication(int resultItemTypes, boolean enabled)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`enabled` Set whether to enable result result deduplication.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### isResultDeduplicationEnabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```java
boolean isResultDeduplicationEnabled(@EnumCapturedResultItemType int type)
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a boolean value indicating whether result deduplication is enabled for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### setDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types.

```java
void setDuplicateForgetTime(int resultItemTypes, int time)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`time` The duplicate forget time in milliseconds.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### getDuplicateForgetTime

Gets the duplicate forget time for a specific captured result item type.

```java
int getDuplicateForgetTime(@EnumCapturedResultItemType int resultItemTypes)
```

**Parameters**

`resultItemTypes` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns the duplicate forget time in milliseconds for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### setMaxOverlappingFrames

Sets the max referencing frames count for the to-the-latest overlapping feature.

```java
void setMaxOverlappingFrames(int resultItemTypes, int maxOverlappingFrames)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`maxOverlappingFrames` The max referencing frames count.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### getMaxOverlappingFrames

Gets the max referencing frames count for the to-the-latest overlapping feature.

```java
int getMaxOverlappingFrames(@EnumCapturedResultItemType int resultItemType)
```

**Parameters**

`resultItemType` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns the max referencing frames count for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### enableLatestOverlapping

Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.

```java
void enableLatestOverlapping(int resultItemTypes, boolean enabled)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`enabled` Set whether to enable the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### is_result_deduplication_enabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```java
def is_result_deduplication_enabled(self, type: int) -> bool:
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a bool value indicating whether result deduplication is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### set_duplicate_forget_time

Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period if deduplication feature is enabled. The default value is 3000ms.

```java
def set_duplicate_forget_time(self, result_item_types: int, time: int) -> None:
```

**Parameters**

`result_item_types` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`time` The duplicate forget time measured in milliseconds. The value rang is [1, 180000].

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### get_duplicate_forget_time

Gets the duplicate forget time for a specific captured result item type.

```java
def get_duplicate_forget_time(self, type: int) -> int:
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns the duplicate forget time for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### set_max_overlapping_frames

Sets the max referencing frames count for the to-the-latest overlapping feature.

```java
def set_max_overlapping_frames(self, result_item_types: int, max_overlapping_frames: int) -> None:
```

**Parameters**

`result_item_types` The or value of the captured result item types.

`max_overlapping_frames` The max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### get_max_overlapping_frames

Gets the max referencing frames count for the to-the-latest overlapping feature.

```java
def get_max_overlapping_frames(self, type: int) -> int:
```

**Parameters**

`type` Specifies a specific result item type, which can be defined using `EnumCapturedResultItemType`.

**Return value**

Returns the max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)


### enable_latest_overlapping

Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.

```java
def enable_latest_overlapping(self, result_item_types: int, enabled: bool) -> None:
```

**Parameters**

`result_item_types` The or value of the captured result item types.  
`enabled` Sets whether to enable the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### is_latest_overlapping_enabled

Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.

```java
def is_latest_overlapping_enabled(self, type: int) -> bool:
```

**Parameters**

`type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether the to-the-latest overlapping feature is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)


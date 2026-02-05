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

*Package:* com.dynamsoft.utility

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
| [`isLatestOverlappingEnabled`](#islatestoverlappingenabled) | Determines whether the to-the-latest overlapping feature is enabled for the specific result item type. |
| [`setResultCrossVerificationCriteria`](#setresultcrossverificationcriteria) | Sets the cross-verification criteria for specified result item types. |
| [`getResultCrossVerificationCriteria`](#getresultcrossverificationcriteria) | Gets the cross-verification criteria for a specified result item type. |

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

### isLatestOverlappingEnabled

Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.

```java
boolean isLatestOverlappingEnabled(@EnumCapturedResultItemType int type)
```

**Parameters**

`type` The specific captured result item type. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return Value**

Returns a boolean value indicating whether to-the-latest overlapping is enabled for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### setResultCrossVerificationCriteria

Sets the cross-verification criteria for specified result item types. This method allows customization of the multi-frame verification parameters, controlling how many frames are analyzed and how many consistent results are required.

```java
void setResultCrossVerificationCriteria(int resultItemTypes, int frameWindow, int minConsistentFrames)
```

**Parameters**

`resultItemTypes` A bitwise OR combination of one or more values from the `EnumCapturedResultItemType` enumeration.

`frameWindow` The number of frames to consider for cross-verification.

`minConsistentFrames` The minimum number of frames that must contain consistent results for verification to succeed.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

**Remarks**

Introduced in Dynamsoft Barcode Reader SDK version 11.4.1000 and Dynamsoft Capture Vision version 3.4.1000.

### getResultCrossVerificationCriteria

Gets the cross-verification criteria for a specified result item type.

```java
int[] getResultCrossVerificationCriteria(@EnumCapturedResultItemType int resultItemType)
```

**Parameters**

`resultItemType` The result item type to query. It is a value from the `EnumCapturedResultItemType` enumeration.

**Return value**

Returns an int array where the first element is the frame window size and the second element is the minimum consistent frames count.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

**Remarks**

Introduced in Dynamsoft Barcode Reader SDK version 11.4.1000 and Dynamsoft Capture Vision version 3.4.1000.


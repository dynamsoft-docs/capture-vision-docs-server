---
layout: default-layout
title: class CMultiFrameResultCrossFilter - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CMultiFrameResultCrossFilter in Utility Module.
keywords: multiple frame result cross filter, c++
---

# CMultiFrameResultCrossFilter

The `CMultiFrameResultCrossFilter` class is responsible for filtering captured results. As a default implementation of `CCapturedResultFilter`, it provides results verification and duplicate results filtering features.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CMultiFrameResultCrossFilter: public CCapturedResultFilter
```

## Methods Summary

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`EnableResultCrossVerification`](#enableresultcrossverification)               | Enable result cross verification feature to improve the accuracy of video streaming recognition results.                                          |
| [`IsResultCrossVerificationEnabled`](#isresultcrossverificationenabled)              | Determines whether the result cross verification feature is enabled for the specific captured result item type.                                           |
| [`EnableResultDeduplication`](#enableresultdeduplication)       | Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.              |
| [`IsResultDeduplicationEnabled`](#isresultdeduplicationenabled)           | Determines whether the result deduplication feature is enabled for the specific result item type.          |
| [`SetDuplicateForgetTime`](#setduplicateforgettime)           | Sets the duplicate forget time for the specific captured result item types.             |
| [`GetDuplicateForgetTime`](#getduplicateforgettime)         | Gets the duplicate forget time for a specific captured result item type.     |
| [`SetMaxOverlappingFrames`](#setmaxoverlappingframes)           | Sets the max referencing frames count for the to-the-latest overlapping feature.             |
| [`GetMaxOverlappingFrames`](#getmaxoverlappingframes)         | Gets the max referencing frames count for the to-the-latest overlapping feature.     |
| [`EnableLatestOverlapping`](#enablelatestoverlapping)               | Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.                                          |
| [`IsLatestOverlappingEnabled`](#islatestoverlappingenabled)              | Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.                                           |

### EnableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```cpp
void EnableResultCrossVerification(int resultItemTypes, bool enabled);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Sets whether to enable result verification.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### IsResultCrossVerificationEnabled

Determines whether the result cross verification feature is enabled for the specific captured result item type.

```cpp
bool IsResultCrossVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether result verification is enabled for the specific captured result item type.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### EnableResultDeduplication

Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.  The default value of `duplicateForgetTime` is 3000ms.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```cpp
void EnableResultDeduplication(int resultItemTypes, bool enabled);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Sets whether to enable result result deduplication.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### IsResultDeduplicationEnabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```cpp
bool IsResultDeduplicationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether result deduplication is enabled for the specific result item type.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### SetDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```cpp
void SetDuplicateForgetTime(int resultItemTypes, int time);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] time` The duplicate forget time measured in milliseconds. The value rang is [1, 180000].

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### GetDuplicateForgetTime

Gets the duplicate forget time for a specific captured result item type.

```cpp
int GetDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns the duplicate forget time for the specific captured result item type.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### SetMaxOverlappingFrames

Sets the max referencing frames count for the to-the-latest overlapping feature.

```cpp
void SetMaxOverlappingFrames(int resultItemTypes, int maxOverlappingFrames);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.

`[in] maxOverlappingFrames` The max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### GetMaxOverlappingFrames

Gets the max referencing frames count for the to-the-latest overlapping feature.

```cpp
int GetMaxOverlappingFrames(CapturedResultItemType resultItemType) const;
```

**Parameters**

`[in] resultItemType` Specifies a specific result item type, which can be defined using `CapturedResultItemType`.

**Return value**

Returns the max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)


### EnableLatestOverlapping

Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.

```cpp
void EnableLatestOverlapping(int resultItemTypes, bool enabled);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Sets whether to enable the to-the-latest overlapping feature.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### IsLatestOverlappingEnabled

Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.

```cpp
bool IsLatestOverlappingEnabled(CapturedResultItemType type) const;
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether the to-the-latest overlapping feature is enabled for the specific result item type.

**See Also**

[CapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

---
layout: default-layout
title: class CMultiFrameResultCrossFilter - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CMultiFrameResultCrossFilter in Utility Module.
keywords: multiple frame result cross filter, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CMultiFrameResultCrossFilter Class
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

### EnableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```cpp
void EnableResultCrossVerification(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enable` Set whether to enable result verification.

### IsResultCrossVerificationEnabled

Determines whether the result cross verification feature is enabled for the specific captured result item type.

```cpp
bool IsResultCrossVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether result verification is enabled for the specific captured result item type.

### EnableResultDeduplication

Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.  The default value of `duplicateForgetTime` is 3000ms.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```cpp
void EnableResultDeduplication(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enable` Set whether to enable result result deduplication.

### IsResultDeduplicationEnabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```cpp
bool IsResultDeduplicationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether result deduplication is enabled for the specific result item type.

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

### GetDuplicateForgetTime

Gets the duplicate forget time for a specific captured result item type.

```cpp
int GetDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns the duplicate forget time for the specific captured result item type.

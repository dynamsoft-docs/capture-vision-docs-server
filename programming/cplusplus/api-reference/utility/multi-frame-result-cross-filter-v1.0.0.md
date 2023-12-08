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
| [`EnableResultVerification`](#enableresultverification)               | Enable result verification feature to improve the accuracy of video streaming recognition results.                                          |
| [`IsResultVerificationEnabled`](#isresultverificationenabled)              | Determines whether the result verification feature is enabled for the specific captured result item type.                                           |
| [`EnableDuplicateFilter`](#enableduplicatefilter)       | Enable duplicate filter feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.              |
| [`IsDuplicateFilterEnabled`](#isduplicatefilterenabled)           | Determines whether the duplicate filter feature is enabled for the specific result item type.          |
| [`SetDuplicateForgetTime`](#setduplicateforgettime)           | Sets the duplicate forget time for the specific captured result item types.             |
| [`GetDuplicateForgetTime`](#getduplicateforgettime)         | Gets the duplicate forget time for a specific captured result item type.     |

### EnableResultVerification

Enable result verification feature to improve the accuracy of video streaming recognition results.

```cpp
void EnableResultVerification(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enable` Set whether to enable result verification.

### IsResultVerificationEnabled

Determines whether the result verification feature is enabled for the specific captured result item type.

```cpp
bool IsResultVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether result verification is enabled for the specific captured result item type.

### EnableDuplicateFilter

Enable duplicate filter feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.  The default value of `duplicateForgetTime` is 3000ms.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```cpp
void EnableDuplicateFilter(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enable` Set whether to enable result duplicate filter.

### IsDuplicateFilterEnabled

Determines whether the duplicate filter feature is enabled for the specific result item type.

```cpp
bool IsDuplicateFilterEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether duplicate filter is enabled for the specific result item type.

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
`[in] time` The duplicate forget time measured in milliseconds.

### GetDuplicateForgetTime

Gets the duplicate forget time for a specific captured result item type.

```cpp
int GetDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns the duplicate forget time for the specific captured result item type.

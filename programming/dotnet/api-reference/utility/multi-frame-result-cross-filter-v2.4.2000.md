---
layout: default-layout
title: MultiFrameResultCrossFilter Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of MultiFrameResultCrossFilter class in Dynamsoft Utility Module .NET Edition.
keywords: multiple frame result cross filter, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class is responsible for filtering captured results. As a default implementation of `CapturedResultFilter`, it provides results verification and duplicate results filtering features.

## Definition

*Namespace:* Dynamsoft.Utility

*Assembly:* Dynamsoft.Utility.dll

*Inheritance:* [CapturedResultFilter]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) -> MultiFrameResultCrossFilter

```csharp
public class MultiFrameResultCrossFilter : CapturedResultFilter
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`MultiFrameResultCrossFilter`](#multiframeresultcrossfilter) | Default constructor of a `MultiFrameResultCrossFilter` object. |
| [`EnableResultCrossVerification`](#enableresultcrossverification) | Enable result cross verification feature to improve the accuracy of video streaming recognition results. |
| [`IsResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Determines whether the result cross verification feature is enabled for the specific captured result item type. |
| [`EnableResultDeduplication`](#enableresultdeduplication) | Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition. |
| [`IsResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Determines whether the result deduplication feature is enabled for the specific result item type. |
| [`SetDuplicateForgetTime`](#setduplicateforgettime) | Sets the duplicate forget time for the specific captured result item types. |
| [`GetDuplicateForgetTime`](#getduplicateforgettime) | Gets the duplicate forget time for a specific captured result item type. |
| [`SetMaxOverlappingFrames`](#setmaxoverlappingframes) | Sets the max referencing frames count for the to-the-latest overlapping feature. |
| [`GetMaxOverlappingFrames`](#getmaxoverlappingframes) | Gets the max referencing frames count for the to-the-latest overlapping feature. |
| [`EnableLatestOverlapping`](#enablelatestoverlapping) | Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous. |
| [`IsLatestOverlappingEnabled`](#islatestoverlappingenabled) | Determines whether the to-the-latest overlapping feature is enabled for the specific result item type. |
| [`Dispose`](#dispose) | Releases all resources used by current object. |

### MultiFrameResultCrossFilter

Default constructor of a `MultiFrameResultCrossFilter` object.

```csharp
MultiFrameResultCrossFilter()
```

### EnableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```csharp
void EnableResultCrossVerification(int resultItemTypes, bool enabled)
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Set whether to enable result verification.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### IsResultCrossVerificationEnabled

Determines whether the result cross verification feature is enabled for the specific captured result item type.

```csharp
bool IsResultCrossVerificationEnabled(EnumCapturedResultItemType type)
```

**Parameters**

`[in] type` The specific captured result item type.

**Return Value**

Returns a bool value indicating whether result verification is enabled for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### EnableResultDeduplication

Enable result deduplication feature to filter out the duplicate results in the period of `duplicateForgetTime` for video streaming recognition.  The default value of `duplicateForgetTime` is 3000ms.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```csharp
void EnableResultDeduplication(int resultItemTypes, bool enabled)
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Set whether to enable result result deduplication.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### IsResultDeduplicationEnabled

Determines whether the result deduplication feature is enabled for the specific result item type.

```csharp
bool IsResultDeduplicationEnabled(EnumCapturedResultItemType type)
```

**Parameters**

`[in] type` The specific captured result item type.

**Return Value**

Returns a bool value indicating whether result deduplication is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### SetDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types. The same captured result item will be returned only once during the period.

- CRIT_BARCODE: When the text and format are identical, it is considered as the same barcode.
- CRIT_TEXT_LINE: When the text is exactly the same, it is considered as the same text line.
- CRIT_DETECTED_QUAD: When the quadrilateral is approximately the same, it is considered as the same quadrilateral.

```csharp
void SetDuplicateForgetTime(int resultItemTypes, int time)
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] time` The duplicate forget time measured in milliseconds. The value rang is [1, 180000].

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### GetDuplicateForgetTime

Gets the duplicate forget time for a specific captured result item type.

```csharp
int GetDuplicateForgetTime(EnumCapturedResultItemType type)
```

**Parameters**

`[in] type` The specific captured result item type.

**Return Value**

Returns the duplicate forget time for the specific captured result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### SetMaxOverlappingFrames

Sets the max referencing frames count for the to-the-latest overlapping feature.

```csharp
void SetMaxOverlappingFrames(int resultItemTypes, int maxOverlappingFrames);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.

`[in] maxOverlappingFrames` The max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### GetMaxOverlappingFrames

Gets the max referencing frames count for the to-the-latest overlapping feature.

```csharp
int GetMaxOverlappingFrames(EnumCapturedResultItemType resultItemType)
```

**Parameters**

`[in] resultItemType` Specifies a specific result item type, which can be defined using `EnumCapturedResultItemType`.

**Return value**

Returns the max referencing frames count for the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)


### EnableLatestOverlapping

Enables the to-the-latest overlapping feature. The output captured result will become a combination of the recent results if the latest frame is proved to be similar with the previous.

```csharp
void EnableLatestOverlapping(int resultItemTypes, bool enabled);
```

**Parameters**

`[in] resultItemTypes` The or value of the captured result item types.  
`[in] enabled` Sets whether to enable the to-the-latest overlapping feature.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### IsLatestOverlappingEnabled

Determines whether the to-the-latest overlapping feature is enabled for the specific result item type.

```csharp
bool IsLatestOverlappingEnabled(EnumCapturedResultItemType type)
```

**Parameters**

`[in] type` The specific captured result item type.

**Return value**

Returns a bool value indicating whether the to-the-latest overlapping feature is enabled for the specific result item type.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### Dispose

Releases all resources used by current object.

```csharp
override void Dispose()
```

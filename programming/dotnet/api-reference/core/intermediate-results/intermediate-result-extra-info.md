---
layout: default-layout
title: class IntermediateResultExtraInfo - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the struct IntermediateResultExtraInfo in Dynamsoft Core Module.
keywords: intermediate result, .NET
needAutoGenerateSidebar: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` class represents the extra information for generating an intermediate result unit.

## Definition


```csharp
class IntermediateResultExtraInfo
```

## Attributes Summary

| Attribute                                             | Type                                |
| ----------------------------------------------------- | ----------------------------------- |
| [`targetROIDefName`](#targetroidefname)               | *string*                      |
| [`taskName`](#taskname)                               | *string*                      |
| [`isSectionLevelResult`](#issectionlevelresult)       | *bool*                              |
| [`sectionType`](#sectiontype)                         | *EnumSectionType*                       |

### targetROIDefName

Specifies the name of the `TargetROIDef` object that generates the intermediate result.

```csharp
string targetROIDefName
```

### taskName

Specifies the name of the task that generates the intermediate result.

```csharp
string taskName
```

### isSectionLevelResult

Specifies whether the intermediate result is section-level result.

```csharp
bool isSectionLevelResult
```

### sectionType

Specifies the `SectionType` that generates the intermediate result.

```csharp
EnumSectionType sectionType
```

**See Also**

[EnumSectionType]({{ site.dcvb_dotnet_api }}core/enum-section-type.html)


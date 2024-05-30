---
layout: default-layout
title: CapturedResultItem Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of CapturedResultItem class in Dynamsoft Core Module .NET Edition.
keywords: captured result item, .NET
needAutoGenerateSidebar: true
---

# CapturedResultItem

The `CapturedResultItem` class represents an item in a captured result. It is an abstract base class with multiple subclasses, each representing a different type of captured item such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public abstract class CapturedResultItem 
```

## Methods

| Method                         | Description|
|--------------------------------|------------|
| [`GetCapturedResultItemType`](#getcapturedresultitemtype)              | Gets the type of the captured result item. |
| [`GetReferencedItem`](#getreferenceditem)    | Gets a pointer to the referenced item in the captured result. |
| [`GetTargetROIDefName`](#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`GetTaskName`](#gettaskname) | Gets the name of the task. |

### GetCapturedResultItemType

Gets the type of the captured result item.

```csharp
abstract EnumCapturedResultItemType GetCapturedResultItemType()
```

**Return Value**

Returns the type of the captured result item.

**See Also**

[EnumCapturedResultItemType]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### GetReferencedItem

Gets the referenced item in the captured result item.

```csharp
abstract CapturedResultItem GetReferencedItem()
```

**Return Value**

Returns a referenced item in the captured result item.

**See Also**

[CapturedResultItem]({{ site.dcv_dotnet_api }}core/basic-classes/captured-result-item.html)

### GetTargetROIDefName

Gets the name of the target ROI definition.

```csharp
string GetTargetROIDefName()
```

**Return Value**

Returns the name of the target ROI definition.

### GetTaskName

Gets the name of the task.

```csharp
string GetTaskName()
```

**Return Value**

Returns the name of the task.

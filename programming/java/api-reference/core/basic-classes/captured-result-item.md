---
layout: default-layout
title: CapturedResultItem Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of CapturedResultItem class in Dynamsoft Core Module Java Edition.
keywords: captured result item, java
needAutoGenerateSidebar: true
---

# CapturedResultItem

The `CapturedResultItem` class represents an item in a captured result. It is an abstract base class with multiple subclasses, each representing a different type of captured item such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Package:* com.dynamsoft.core.basic_structures

```java
public class CapturedResultItem
```

## Methods

| Method                         | Description|
|--------------------------------|------------|
| [`getType`](#gettype)              | Gets the type of the captured result item. |
| [`getReferenceItem`](#getreferenceitem)    | Gets the referenced item in the captured result. |
| [`getTargetROIDefName`](#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`getTaskName`](#gettaskname) | Gets the name of the task. |

### getType

Gets the type of the captured result item.

```java
public @EnumCapturedResultItemType int getType()
```

**Return Value**

Returns the type of the captured result item.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_java_api }}core/enum-captured-result-item-type.html)

### getReferenceItem

Gets the referenced item in the captured result item.

```java
public CapturedResultItem getReferenceItem()
```

**Return Value**

Returns a referenced item in the captured result item.

**See Also**

[CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html)

### getTargetROIDefName

Gets the name of the target ROI definition.

```java
public String getTargetROIDefName()
```

**Return Value**

Returns the name of the target ROI definition.

### getTaskName

Gets the name of the task.

```java
public String getTaskName()
```

**Return Value**

Returns the name of the task.

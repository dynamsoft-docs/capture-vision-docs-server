---
layout: default-layout
title: CapturedResultItem Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of CapturedResultItem class in Dynamsoft Core Module Python Edition.
keywords: captured result item, python
needAutoGenerateSidebar: true
---

# CapturedResultItem

The `CapturedResultItem` class represents an item in a captured result. It is an abstract base class with multiple subclasses, each representing a different type of captured item such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Module:* dynamsoft_core

```python
class CapturedResultItem
```

## Methods

| Method                         | Description|
|--------------------------------|------------|
| [`get_type`](#get_type)              | Gets the type of the captured result item. |
| [`get_reference_item`](#get_reference_item)    | Gets the referenced item in the captured result. |
| [`get_target_roi_def_name`](#get_target_roi_def_name) | Gets the name of the target ROI definition. |
| [`get_task_name`](#get_task_name) | Gets the name of the task. |

### get_type

Gets the type of the captured result item.

```python
def get_type(self) -> int:
```

**Return Value**

Returns the type of the captured result item.

**See Also**

[EnumCapturedResultItemType]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)

### get_reference_item

Gets the referenced item in the captured result item.

```python
def get_reference_item(self) -> "CapturedResultItem":
```

**Return Value**

Returns a referenced item in the captured result item.

**See Also**

[CapturedResultItem]({{ site.dcvb_python_api }}core/basic-classes/captured-result-item.html)

### get_target_roi_def_name

Gets the name of the target ROI definition.

```python
def get_target_roi_def_name(self) -> str:
```

**Return Value**

Returns the name of the target ROI definition.

### get_task_name

Gets the name of the task.

```python
def get_task_name(self) -> str:
```

**Return Value**

Returns the name of the task.

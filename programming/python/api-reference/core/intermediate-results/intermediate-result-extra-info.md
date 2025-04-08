---
layout: default-layout
title: struct IntermediateResultExtraInfo - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the struct IntermediateResultExtraInfo in Dynamsoft Core Module.
keywords: intermediate result, python
needAutoGenerateSidebar: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` structure represents the extra information for generating an intermediate result unit.

## Definition

*Module:* dynamsoft_core

```python
class IntermediateResultExtraInfo
```

## Properties

| Attribute                                             | Type    | Description |
| ----------------------------------------------------- | ------- | ----------- |
| [`__init__`](#__init__) | Initializes a new instance of the `IntermediateResultExtraInfo` class. |
| [`target_roi_def_name`](#target_roi_def_name)         | *str*   | Specifies the name of the `TargetROIDef` object that generates the intermediate result. |
| [`task_name`](#task_name)                             | *str*   | Specifies the name of the task that generates the intermediate result. |
| [`is_section_level_result`](#is_section_level_result) | *bool*  | Specifies whether the intermediate result is section-level result. |
| [`section_type`](#section_type)                       | *int*   | Specifies the section_type that generates the intermediate result. This is one of the values of the [EnumSectionType]({{ site.dcvb_python_api }}core/enum-section-type.html) enumeration. |

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `IntermediateResultExtraInfo` class. |

### \_\_init\_\_

Initializes a new instance of the `IntermediateResultExtraInfo` class.

```python
def __init__(self):
```

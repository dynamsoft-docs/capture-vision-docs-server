---
layout: default-layout
title: CapturedResultFilter Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CapturedResultFilter class in Dynamsoft Capture Vision Module Python Edition.
keywords: captured result receiver, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultFilter

The `CapturedResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

>Note: Currently, user defined `CapturedResultFilter` is not supported.

## Definition

*Module:* cvr

```python
class CapturedResultFilter 
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`get_name`](#get_name)       | Gets the name of the captured result filter.                                             |
| [`set_name`](#set_name)       | Sets the name of the captured result filter.                                             |


### get_name

Gets the name of the captured result filter.  

```python
def get_name(self) -> str:
```

**Return Value**

Returns the name of the captured result filter.  

### set_name

Sets the name of the captured result filter.  

```python
def set_name(self, name: str) -> None:
```

**Parameters**

`name` The name of the captured result filter.

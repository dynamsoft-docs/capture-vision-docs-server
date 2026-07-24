---
layout: default-layout
title: LayoutAnalysisResult Class - Dynamsoft Utility Python Edition API Reference
description: API reference for the LayoutAnalysisResult class in Dynamsoft Utility Python Edition, providing comprehensive results of a quadrilateral layout analysis.
keywords: LayoutAnalysisResult, layout analysis, result, inferred quads, python
needAutoGenerateSidebar: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` class holds the comprehensive results of the layout analysis.

## Definition

*Module:* utility

```python
class LayoutAnalysisResult:
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`inferred_quads`](#inferred_quads) | *List[Quadrilateral]* | Array of newly generated (inferred) quads. |
| [`elements`](#elements) | *List[List[LayoutElement]]* | A 2D array (grid) of layout elements. |
| [`row_count`](#row_count) | *int* | Number of rows (Primary Axis direction). |
| [`col_count`](#col_count) | *int* | Maximum number of columns across all rows (Secondary Axis direction). |
| [`detected_pattern`](#detected_pattern) | *EnumLayoutPattern* | The actual layout pattern identified by the engine. |
| [`error_code`](#error_code) | *int* | 0 for success, non-zero for error. |

### inferred_quads

Array of newly generated (inferred) quads.

```python
inferred_quads: List[Quadrilateral]
```

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### elements

A 2D array (grid) of layout elements `[row_count][col_count]`. In `LP_LINES` mode, rows may have varying physical lengths. Rows shorter than `col_count` are padded with elements whose source is set to `LES_NONE`.

```python
elements: List[List[LayoutElement]]
```

**See Also**

[LayoutElement]({{ site.dcvb_python_api }}utility/layout-element.html)

### row_count

Number of rows (Primary Axis direction).

```python
row_count: int
```

### col_count

Maximum number of columns across all rows (Secondary Axis direction).

```python
col_count: int
```

### detected_pattern

The actual layout pattern identified by the engine.

```python
detected_pattern: EnumLayoutPattern
```

**See Also**

[EnumLayoutPattern]({{ site.dcvb_python_api }}utility/enum-layout-pattern.html)

### error_code

0 for success, non-zero for error.

```python
error_code: int
```

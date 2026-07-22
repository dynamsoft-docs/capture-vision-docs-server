---
layout: default-layout
title: LayoutAnalysisParameter Class - Dynamsoft Utility Python Edition API Reference
description: API reference for the LayoutAnalysisParameter class in Dynamsoft Utility Python Edition, providing input parameters to guide quadrilateral layout analysis.
keywords: LayoutAnalysisParameter, layout analysis, parameter, python
needAutoGenerateSidebar: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` class holds input parameters to guide the layout analysis.

## Definition

*Module:* utility

```python
class LayoutAnalysisParameter:
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`pattern`](#pattern) | *EnumLayoutPattern* | Desired layout pattern. |
| [`axes`](#axes) | *List[LayoutAxis]* | Configuration for Primary (0) and Secondary (1) axes. |
| [`input_image_width`](#input_image_width) | *int* | Width of the source image in pixels. |
| [`input_image_height`](#input_image_height) | *int* | Height of the source image in pixels. |

### pattern

Desired layout pattern. Use `LP_UNKNOWN` for auto-detection.

```python
pattern: EnumLayoutPattern
```

**See Also**

[EnumLayoutPattern]({{ site.dcvb_python_api }}utility/enum-layout-pattern.html)

### axes

Configuration for Primary (axis 0) and Secondary (axis 1) axes.

```python
axes: List[LayoutAxis]
```

**See Also**

[LayoutAxis]({{ site.dcvb_python_api }}utility/layout-axis.html)

### input_image_width

Width of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```python
input_image_width: int
```

### input_image_height

Height of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```python
input_image_height: int
```

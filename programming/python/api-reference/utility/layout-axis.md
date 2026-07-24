---
layout: default-layout
title: LayoutAxis Class - Dynamsoft Utility Python Edition API Reference
description: API reference for the LayoutAxis class in Dynamsoft Utility Python Edition, configuring axis parameters for quadrilateral layout analysis.
keywords: LayoutAxis, layout axis, spacing, angle, staggered, python
needAutoGenerateSidebar: true
---

# LayoutAxis

The `LayoutAxis` class holds configuration for a specific orientation axis used in layout analysis. Layout analysis involves two axes:

- **Axis 0 (Primary)**: The direction of flow within a line.
- **Axis 1 (Secondary)**: The direction in which lines are stacked.

## Definition

*Module:* utility

```python
class LayoutAxis:
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`element_count`](#element_count) | *int* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`is_staggered`](#is_staggered) | *bool* | Whether the layout uses an offset/staggered (brick-like) pattern. |
| [`angle`](#angle) | *int* | Target angle in degrees [0, 180]. Use -1 for auto-detection. |
| [`is_equal_spacing`](#is_equal_spacing) | *bool* | Force equal gaps between elements. |
| [`spacing`](#spacing) | *int* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacing_unit`](#spacing_unit) | *EnumMeasureUnit* | Interpretation mode for the spacing value. |

### element_count

```python
element_count: int
```

### is_staggered

```python
is_staggered: bool
```

### angle

```python
angle: int
```

### is_equal_spacing

```python
is_equal_spacing: bool
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

- In `MU_PIXEL` mode: absolute pixel count.
- In `MU_PERCENTAGE` mode: percentage of the element's characteristic size (e.g., 200 = 200% = twice the reference width).

```python
spacing: int
```

### spacing_unit

```python
spacing_unit: EnumMeasureUnit
```

**See Also**

[EnumMeasureUnit]({{ site.dcvb_python_api }}core/enum-measure-unit.html)

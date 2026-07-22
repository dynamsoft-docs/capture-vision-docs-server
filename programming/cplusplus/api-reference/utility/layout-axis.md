---
layout: default-layout
title: LayoutAxis - Dynamsoft Utility C++ Edition API Reference
description: API reference for the LayoutAxis structure in Dynamsoft Utility C++ Edition, configuring axis parameters for quadrilateral layout analysis.
keywords: LayoutAxis, layout axis, spacing, angle, staggered
needAutoGenerateSidebar: true
---

# LayoutAxis

The `LayoutAxis` structure holds configuration for a specific orientation axis used in layout analysis. Layout analysis involves two axes:

- **Axis 0 (Primary)**: The direction of flow within a line.
- **Axis 1 (Secondary)**: The direction in which lines are stacked.

## Definition

*Assembly:* DynamsoftUtility

*Header File:* DynamsoftUtility.h

```cpp
typedef struct LayoutAxis
{
    int elementCount;
    bool isStaggered;
    int angle;
    bool isEqualSpacing;
    int spacing;
    MeasureUnit spacingUnit;
    char reserved[32];
} LayoutAxis;
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`elementCount`](#elementcount) | *int* | Expected number of elements along this axis. |
| [`isStaggered`](#isstaggered) | *bool* | Whether the layout uses an offset/staggered (brick-like) pattern. |
| [`angle`](#angle) | *int* | Target angle in degrees [0, 180]. |
| [`isEqualSpacing`](#isequalspaing) | *bool* | Force equal gaps between elements. |
| [`spacing`](#spacing) | *int* | Spacing between elements along this axis. |
| [`spacingUnit`](#spacingunit) | *MeasureUnit* | Interpretation mode for the spacing value. |

### elementCount

Expected number of elements along this axis. Use -1 for auto-detection.

```cpp
int elementCount = -1;
```

### isStaggered

Whether the layout uses an offset/staggered (brick-like) pattern.

```cpp
bool isStaggered = false;
```

### angle

Target angle in degrees [0, 180]. Use -1 for auto-detection.

```cpp
int angle = -1;
```

### isEqualSpacing

Force equal gaps between elements. When false, spacing is ignored.

```cpp
bool isEqualSpacing = false;
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

- In `MU_PIXEL` mode: absolute pixel count.
- In `MU_PERCENTAGE` mode: percentage of the element's characteristic size (e.g., 200 = 200% = twice the reference width).

```cpp
int spacing = -1;
```

### spacingUnit

Interpretation mode for the spacing value.

```cpp
MeasureUnit spacingUnit = MU_PIXEL;
```

**See Also**

[MeasureUnit]({{ site.dcvb_cpp_api }}core/enum-measure-unit.html?lang=cpp)

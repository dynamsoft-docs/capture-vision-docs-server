---
layout: default-layout
title: LayoutAxis Class - Dynamsoft Utility Java Edition API Reference
description: API reference for the LayoutAxis class in Dynamsoft Utility Java Edition, configuring axis parameters for quadrilateral layout analysis.
keywords: LayoutAxis, layout axis, spacing, angle, staggered, java
needAutoGenerateSidebar: true
---

# LayoutAxis

The `LayoutAxis` class holds configuration for a specific orientation axis used in layout analysis. Layout analysis involves two axes:

- **Axis 0 (Primary)**: The direction of flow within a line.
- **Axis 1 (Secondary)**: The direction in which lines are stacked.

## Definition

*Package:* `com.dynamsoft.utility`

```java
class LayoutAxis
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`elementCount`](#elementcount) | *int* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`isStaggered`](#isstaggered) | *boolean* | Whether the layout uses an offset/staggered (brick-like) pattern. |
| [`angle`](#angle) | *int* | Target angle in degrees [0, 180]. Use -1 for auto-detection. |
| [`isEqualSpacing`](#isequalspaing) | *boolean* | Force equal gaps between elements. |
| [`spacing`](#spacing) | *int* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacingUnit`](#spacingunit) | *int* | Interpretation mode for the spacing value. |

### elementCount

```java
public int elementCount = -1;
```

### isStaggered

```java
public boolean isStaggered = false;
```

### angle

```java
public int angle = -1;
```

### isEqualSpacing

```java
public boolean isEqualSpacing = false;
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

- In `MU_PIXEL` mode: absolute pixel count.
- In `MU_PERCENTAGE` mode: percentage of the element's characteristic size (e.g., 200 = 200% = twice the reference width).

```java
public int spacing = -1;
```

### spacingUnit

```java
public @EnumMeasureUnit int spacingUnit = EnumMeasureUnit.MU_PIXEL;
```

**See Also**

[EnumMeasureUnit]({{ site.dcvb_java_api }}core/enum-measure-unit.html)

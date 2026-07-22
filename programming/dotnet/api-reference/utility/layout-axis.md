---
layout: default-layout
title: LayoutAxis Class - Dynamsoft Utility .NET Edition API Reference
description: API reference for the LayoutAxis class in Dynamsoft Utility .NET Edition, configuring axis parameters for quadrilateral layout analysis.
keywords: LayoutAxis, layout axis, spacing, angle, staggered
needAutoGenerateSidebar: true
---

# LayoutAxis

The `LayoutAxis` class holds configuration for a specific orientation axis used in layout analysis. Layout analysis involves two axes:

- **Axis 0 (Primary)**: The direction of flow within a line.
- **Axis 1 (Secondary)**: The direction in which lines are stacked.

## Definition

*Namespace:* Dynamsoft.Utility

```csharp
public class LayoutAxis
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`elementCount`](#elementcount) | *int* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`isStaggered`](#isstaggered) | *bool* | Whether the layout uses an offset/staggered (brick-like) pattern. |
| [`angle`](#angle) | *int* | Target angle in degrees [0, 180]. Use -1 for auto-detection. |
| [`isEqualSpacing`](#isequalspaing) | *bool* | Force equal gaps between elements. |
| [`spacing`](#spacing) | *int* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacingUnit`](#spacingunit) | *MeasureUnit* | Interpretation mode for the spacing value. |

### elementCount

```csharp
public int elementCount = -1;
```

### isStaggered

```csharp
public bool isStaggered = false;
```

### angle

```csharp
public int angle = -1;
```

### isEqualSpacing

```csharp
public bool isEqualSpacing = false;
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

- In `MU_PIXEL` mode: absolute pixel count.
- In `MU_PERCENTAGE` mode: percentage of the element's characteristic size (e.g., 200 = 200% = twice the reference width).

```csharp
public int spacing = -1;
```

### spacingUnit

```csharp
public MeasureUnit spacingUnit = MeasureUnit.MU_PIXEL;
```

**See Also**

[MeasureUnit]({{ site.dcvb_dotnet_api }}core/enum-measure-unit.html)

---
layout: default-layout
title: LayoutAnalysisParameter - Dynamsoft Utility C++ Edition API Reference
description: API reference for the LayoutAnalysisParameter structure in Dynamsoft Utility C++ Edition, providing input parameters to guide quadrilateral layout analysis.
keywords: LayoutAnalysisParameter, layout analysis, parameter
needAutoGenerateSidebar: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` structure holds input parameters to guide the layout analysis.

## Definition

*Assembly:* DynamsoftUtility

*Header File:* DynamsoftUtility.h

```cpp
typedef struct LayoutAnalysisParameter
{
    LayoutPattern pattern;
    LayoutAxis axes[2];
    int inputImageWidth;
    int inputImageHeight;
    char reserved[32];
} LayoutAnalysisParameter;
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`pattern`](#pattern) | *LayoutPattern* | Desired layout pattern. |
| [`axes`](#axes) | *LayoutAxis[2]* | Configuration for Primary (0) and Secondary (1) axes. |
| [`inputImageWidth`](#inputimagewidth) | *int* | Width of the source image in pixels. |
| [`inputImageHeight`](#inputimageheight) | *int* | Height of the source image in pixels. |

### pattern

Desired layout pattern. Use `LP_UNKNOWN` for auto-detection.

```cpp
LayoutPattern pattern = LP_UNKNOWN;
```

**See Also**

[LayoutPattern]({{ site.dcvb_cpp_api }}utility/enum-layout-pattern.html?lang=cpp)

### axes

Configuration for Primary (axis 0) and Secondary (axis 1) axes.

```cpp
LayoutAxis axes[2];
```

**See Also**

[LayoutAxis]({{ site.dcvb_cpp_api }}utility/layout-axis.html)

### inputImageWidth

Width of the source image in pixels. When provided, the engine uses this as a boundary reference to prevent inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```cpp
int inputImageWidth = 0;
```

### inputImageHeight

Height of the source image in pixels. When provided, the engine uses this as a boundary reference to prevent inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```cpp
int inputImageHeight = 0;
```

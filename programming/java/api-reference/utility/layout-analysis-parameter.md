---
layout: default-layout
title: LayoutAnalysisParameter Class - Dynamsoft Utility Java Edition API Reference
description: API reference for the LayoutAnalysisParameter class in Dynamsoft Utility Java Edition, providing input parameters to guide quadrilateral layout analysis.
keywords: LayoutAnalysisParameter, layout analysis, parameter, java
needAutoGenerateSidebar: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` class holds input parameters to guide the layout analysis.

## Definition

*Package:* `com.dynamsoft.utility`

```java
class LayoutAnalysisParameter
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`pattern`](#pattern) | *int* | Desired layout pattern. |
| [`axes`](#axes) | *LayoutAxis[]* | Configuration for Primary (0) and Secondary (1) axes. |
| [`inputImageWidth`](#inputimagewidth) | *int* | Width of the source image in pixels. |
| [`inputImageHeight`](#inputimageheight) | *int* | Height of the source image in pixels. |

## Constructors

| Constructor | Description |
|-------------|-------------|
| [`LayoutAnalysisParameter()`](#layoutanalysisparameter) | Initializes a new instance with default values. |

### pattern

Desired layout pattern. Use `LP_UNKNOWN` for auto-detection.

```java
public @EnumLayoutPattern int pattern = EnumLayoutPattern.LP_UNKNOWN;
```

**See Also**

[EnumLayoutPattern]({{ site.dcvb_java_api }}utility/enum-layout-pattern.html)

### axes

Configuration for Primary (axis 0) and Secondary (axis 1) axes.

```java
public LayoutAxis[] axes;
```

**See Also**

[LayoutAxis]({{ site.dcvb_java_api }}utility/layout-axis.html)

### inputImageWidth

Width of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```java
public int inputImageWidth = 0;
```

### inputImageHeight

Height of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```java
public int inputImageHeight = 0;
```

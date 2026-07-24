---
layout: default-layout
title: LayoutAnalysisParameter Class - Dynamsoft Utility .NET Edition API Reference
description: API reference for the LayoutAnalysisParameter class in Dynamsoft Utility .NET Edition, providing input parameters to guide quadrilateral layout analysis.
keywords: LayoutAnalysisParameter, layout analysis, parameter
needAutoGenerateSidebar: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` class holds input parameters to guide the layout analysis.

## Definition

*Namespace:* Dynamsoft.Utility

```csharp
public class LayoutAnalysisParameter
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`pattern`](#pattern) | *LayoutPattern* | Desired layout pattern. |
| [`axes`](#axes) | *LayoutAxis[]* | Configuration for Primary (0) and Secondary (1) axes. |
| [`inputImageWidth`](#inputimagewidth) | *int* | Width of the source image in pixels. |
| [`inputImageHeight`](#inputimageheight) | *int* | Height of the source image in pixels. |

### pattern

Desired layout pattern. Use `LP_UNKNOWN` for auto-detection.

```csharp
public LayoutPattern pattern = LayoutPattern.LP_UNKNOWN;
```

**See Also**

[LayoutPattern]({{ site.dcvb_dotnet_api }}utility/enum-layout-pattern.html)

### axes

Configuration for Primary (axis 0) and Secondary (axis 1) axes.

```csharp
public LayoutAxis[] axes;
```

**See Also**

[LayoutAxis]({{ site.dcvb_dotnet_api }}utility/layout-axis.html)

### inputImageWidth

Width of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```csharp
public int inputImageWidth = 0;
```

### inputImageHeight

Height of the source image in pixels. When provided, prevents inferred quads from extending beyond the image bounds. Default: 0 (no boundary check).

```csharp
public int inputImageHeight = 0;
```

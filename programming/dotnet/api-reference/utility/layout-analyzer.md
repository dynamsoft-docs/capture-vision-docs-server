---
layout: default-layout
title: LayoutAnalyzer Class - Dynamsoft Utility .NET Edition API Reference
description: API reference for the LayoutAnalyzer class in Dynamsoft Utility .NET Edition, providing high-performance quadrilateral layout analysis.
keywords: LayoutAnalyzer, layout analysis, quadrilateral, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides a high-performance layout analysis engine. It analyzes the spatial distribution of quadrilaterals to detect and map structural patterns (Lines or Matrix), with logical grid position mapping and gap-filling inference.

## Definition

*Namespace:* Dynamsoft.Utility

```csharp
public static class LayoutAnalyzer
```

## Methods

| Method | Description |
|--------|-------------|
| [`Analyze`](#analyze) | Performs layout analysis on an array of quadrilaterals and returns a result set. |

## Analyze

Performs layout analysis and returns a result set.

```csharp
public static LayoutAnalysisResult? Analyze(Quadrilateral[] input, LayoutAnalysisParameter? parameter = null)
```

**Parameters**

`[in] input` Array of input quadrilaterals.

`[in] parameter` Optional parameters to constrain the analysis.

**Return Value**

Returns a `LayoutAnalysisResult` object, or `null` on failure.

> **Note:** Dispose the returned object after use.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

[LayoutAnalysisParameter]({{ site.dcvb_dotnet_api }}utility/layout-analysis-parameter.html)

[LayoutAnalysisResult]({{ site.dcvb_dotnet_api }}utility/layout-analysis-result.html)

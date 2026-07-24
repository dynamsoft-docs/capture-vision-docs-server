---
layout: default-layout
title: LayoutAnalyzer Class - Dynamsoft Utility Java Edition API Reference
description: API reference for the LayoutAnalyzer class in Dynamsoft Utility Java Edition, providing high-performance quadrilateral layout analysis.
keywords: LayoutAnalyzer, layout analysis, quadrilateral, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides a high-performance layout analysis engine. It analyzes the spatial distribution of quadrilaterals to detect and map structural patterns (Lines or Matrix), with logical grid position mapping and gap-filling inference.

## Definition

*Package:* `com.dynamsoft.utility`

```java
public final class LayoutAnalyzer
```

## Methods

| Method | Description |
|--------|-------------|
| [`analyze`](#analyze) | Performs layout analysis on an array of quadrilaterals and returns a result set. |

## analyze

Performs layout analysis and returns a result set.

```java
public static LayoutAnalysisResult analyze(Quadrilateral[] inputQuads, LayoutAnalysisParameter parameter)
public static LayoutAnalysisResult analyze(Quadrilateral[] inputQuads)
```

**Parameters**

`inputQuads` Array of input quadrilaterals.

`parameter` Optional parameters to constrain the analysis.

**Return Value**

Returns a `LayoutAnalysisResult` object, or `null` on failure.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

[LayoutAnalysisParameter]({{ site.dcvb_java_api }}utility/layout-analysis-parameter.html)

[LayoutAnalysisResult]({{ site.dcvb_java_api }}utility/layout-analysis-result.html)

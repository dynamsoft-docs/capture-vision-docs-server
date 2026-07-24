---
layout: default-layout
title: class CLayoutAnalyzer - Dynamsoft Utility C++ Edition API Reference
description: API reference for the CLayoutAnalyzer class in Dynamsoft Utility C++ Edition, providing high-performance quadrilateral layout analysis.
keywords: CLayoutAnalyzer, layout analysis, quadrilateral, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CLayoutAnalyzer

The `CLayoutAnalyzer` class provides a high-performance layout analysis engine. It analyzes the spatial distribution of quadrilaterals to detect and map structural patterns (Lines or Matrix), with logical grid position mapping and gap-filling inference.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CLayoutAnalyzer
```

## Methods

| Method | Description |
|--------|-------------|
| [`Analyze`](#analyze) | Performs layout analysis on an array of quadrilaterals and returns a result set. |
| [`ReleaseResult`](#releaseresult) | Releases the memory associated with a `LayoutAnalysisResult`. |

## Analyze

Performs layout analysis and allocates a result set.

```cpp
static LayoutAnalysisResult* Analyze(
    const CQuadrilateral inputQuads[],
    int inputQuadCount,
    const LayoutAnalysisParameter* pParam = nullptr
);
```

**Parameters**

`[in] inputQuads` Array of input quadrilaterals.

`[in] inputQuadCount` Number of elements in the input array.

`[in] pParam` Optional parameters to constrain the analysis.

**Return Value**

Returns a pointer to a `LayoutAnalysisResult` object, or `nullptr` on failure.

> **Note:** The caller **must** release the returned pointer via [`ReleaseResult()`](#releaseresult).

**See Also**

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

[LayoutAnalysisParameter]({{ site.dcvb_cpp_api }}utility/layout-analysis-parameter.html)

[LayoutAnalysisResult]({{ site.dcvb_cpp_api }}utility/layout-analysis-result.html)

## ReleaseResult

Releases the memory associated with a `LayoutAnalysisResult`.

```cpp
static void ReleaseResult(LayoutAnalysisResult* pResultSet);
```

**Parameters**

`[in] pResultSet` Pointer to the result set to be destroyed. No-op if `nullptr`.

**See Also**

[LayoutAnalysisResult]({{ site.dcvb_cpp_api }}utility/layout-analysis-result.html)

---
layout: default-layout
title: LayoutAnalyzer Class - Dynamsoft Utility Python Edition API Reference
description: API reference for the LayoutAnalyzer class in Dynamsoft Utility Python Edition, providing high-performance quadrilateral layout analysis.
keywords: LayoutAnalyzer, layout analysis, quadrilateral, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides a high-performance layout analysis engine. It analyzes the spatial distribution of quadrilaterals to detect and map structural patterns (Lines or Matrix), with logical grid position mapping and gap-filling inference.

## Definition

*Module:* utility

```python
class LayoutAnalyzer:
```

## Methods

| Method | Description |
|--------|-------------|
| [`analyze`](#analyze) | Performs layout analysis on an array of quadrilaterals and returns a result set. |

## analyze

Performs layout analysis and returns a result set.

```python
@staticmethod
def analyze(inputQuads: List[Quadrilateral], param: LayoutAnalysisParameter = None) -> LayoutAnalysisResult:
```

**Parameters**

`inputQuads` Array of input quadrilaterals.

`param` Optional parameters to constrain the analysis.

**Return Value**

Returns a `LayoutAnalysisResult` object, or `None` on failure.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

[LayoutAnalysisParameter]({{ site.dcvb_python_api }}utility/layout-analysis-parameter.html)

[LayoutAnalysisResult]({{ site.dcvb_python_api }}utility/layout-analysis-result.html)

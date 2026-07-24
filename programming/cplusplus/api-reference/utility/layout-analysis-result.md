---
layout: default-layout
title: LayoutAnalysisResult - Dynamsoft Utility C++ Edition API Reference
description: API reference for the LayoutAnalysisResult structure in Dynamsoft Utility C++ Edition, providing comprehensive results of a quadrilateral layout analysis.
keywords: LayoutAnalysisResult, layout analysis, result, inferred quads
needAutoGenerateSidebar: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` structure holds comprehensive results of the layout analysis. It is managed by the engine and must be explicitly released via [`CLayoutAnalyzer::ReleaseResult()`](layout-analyzer.html#releaseresult).

## Definition

*Assembly:* DynamsoftUtility

*Header File:* DynamsoftUtility.h

```cpp
typedef struct LayoutAnalysisResult
{
    CQuadrilateral* inferredQuads;
    int inferredQuadCount;
    LayoutElement** elements;
    int rowCount;
    int colCount;
    LayoutPattern detectedPattern;
    int errorCode;
    char reserved[32];
} LayoutAnalysisResult;
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`inferredQuads`](#inferredquads) | *CQuadrilateral\** | Array of newly generated (inferred) quads. |
| [`inferredQuadCount`](#inferredquadcount) | *int* | Total number of inferred quadrilaterals. |
| [`elements`](#elements) | *LayoutElement\*\** | A 2D array (grid) of layout elements. |
| [`rowCount`](#rowcount) | *int* | Number of rows (Primary Axis direction). |
| [`colCount`](#colcount) | *int* | Maximum number of columns across all rows (Secondary Axis direction). |
| [`detectedPattern`](#detectedpattern) | *LayoutPattern* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *int* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated (inferred) quads.

```cpp
CQuadrilateral* inferredQuads;
```

**See Also**

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### inferredQuadCount

Total number of inferred quadrilaterals.

```cpp
int inferredQuadCount;
```

### elements

A 2D array (grid) of layout elements `[rowCount][colCount]`. In `LP_LINES` mode, rows may have varying physical lengths. Rows shorter than `colCount` are padded with elements whose source is set to `LES_NONE`.

```cpp
LayoutElement** elements;
```

**See Also**

[LayoutElement]({{ site.dcvb_cpp_api }}utility/layout-element.html)

### rowCount

Number of rows (Primary Axis direction).

```cpp
int rowCount;
```

### colCount

Maximum number of columns across all rows (Secondary Axis direction).

```cpp
int colCount;
```

### detectedPattern

The actual layout pattern identified by the engine.

```cpp
LayoutPattern detectedPattern;
```

**See Also**

[LayoutPattern]({{ site.dcvb_cpp_api }}utility/enum-layout-pattern.html)

### errorCode

0 for success, non-zero for error.

```cpp
int errorCode;
```

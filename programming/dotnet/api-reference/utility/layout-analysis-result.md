---
layout: default-layout
title: LayoutAnalysisResult Class - Dynamsoft Utility .NET Edition API Reference
description: API reference for the LayoutAnalysisResult class in Dynamsoft Utility .NET Edition, providing comprehensive results of a quadrilateral layout analysis.
keywords: LayoutAnalysisResult, layout analysis, result, inferred quads
needAutoGenerateSidebar: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` class holds the comprehensive results of the layout analysis. It implements `IDisposable` and must be disposed after use.

## Definition

*Namespace:* Dynamsoft.Utility

```csharp
public class LayoutAnalysisResult : IDisposable
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`inferredQuads`](#inferredquads) | *Quadrilateral[]* | Array of newly generated (inferred) quads. |
| [`elements`](#elements) | *LayoutElement[,]* | A 2D array (grid) of layout elements. |
| [`detectedPattern`](#detectedpattern) | *LayoutPattern* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *int* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated (inferred) quads.

```csharp
public Quadrilateral[] inferredQuads;
```

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### elements

A 2D array (grid) of layout elements `[rowCount, colCount]`. In `LP_LINES` mode, rows may have varying physical lengths. Rows shorter than `colCount` are padded with elements whose source is set to `LES_NONE`.

```csharp
public LayoutElement[,] elements;
```

**See Also**

[LayoutElement]({{ site.dcvb_dotnet_api }}utility/layout-element.html)

### detectedPattern

The actual layout pattern identified by the engine.

```csharp
public LayoutPattern detectedPattern;
```

**See Also**

[LayoutPattern]({{ site.dcvb_dotnet_api }}utility/enum-layout-pattern.html)

### errorCode

0 for success, non-zero for error.

```csharp
public int errorCode;
```

---
layout: default-layout
title: LayoutAnalysisResult Class - Dynamsoft Utility Java Edition API Reference
description: API reference for the LayoutAnalysisResult class in Dynamsoft Utility Java Edition, providing comprehensive results of a quadrilateral layout analysis.
keywords: LayoutAnalysisResult, layout analysis, result, inferred quads, java
needAutoGenerateSidebar: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` class holds the comprehensive results of the layout analysis.

## Definition

*Package:* `com.dynamsoft.utility`

```java
class LayoutAnalysisResult
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`inferredQuads`](#inferredquads) | *Quadrilateral[]* | Array of newly generated (inferred) quads. |
| [`elements`](#elements) | *LayoutElement[][]* | A 2D array (grid) of layout elements. |
| [`detectedPattern`](#detectedpattern) | *int* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *int* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated (inferred) quads.

```java
public Quadrilateral[] inferredQuads;
```

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### elements

A 2D array (grid) of layout elements `[rowCount][colCount]`. In `LP_LINES` mode, rows may have varying physical lengths. Rows shorter than `colCount` are padded with elements whose source is set to `LES_NONE`.

```java
public LayoutElement[][] elements;
```

**See Also**

[LayoutElement]({{ site.dcvb_java_api }}utility/layout-element.html)

### detectedPattern

The actual layout pattern identified by the engine.

```java
public @EnumLayoutPattern int detectedPattern;
```

**See Also**

[EnumLayoutPattern]({{ site.dcvb_java_api }}utility/enum-layout-pattern.html)

### errorCode

0 for success, non-zero for error.

```java
public int errorCode;
```

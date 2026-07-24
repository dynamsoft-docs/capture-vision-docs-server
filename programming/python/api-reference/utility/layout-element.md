---
layout: default-layout
title: LayoutElement Class - Dynamsoft Utility Python Edition API Reference
description: API reference for the LayoutElement class in Dynamsoft Utility Python Edition, representing an element in a quadrilateral layout analysis result.
keywords: LayoutElement, layout element, quad, source, python
needAutoGenerateSidebar: true
---

# LayoutElement

The `LayoutElement` class represents an element in a layout result. It combines the element's geometry with its origin information.

## Definition

*Module:* utility

```python
class LayoutElement:
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`quad`](#quad) | *Quadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *EnumLayoutElementSource* | Origin of this element (Input / Inferred / None). |

### quad

```python
quad: Quadrilateral
```

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### source

```python
source: EnumLayoutElementSource
```

**See Also**

[EnumLayoutElementSource]({{ site.dcvb_python_api }}utility/enum-layout-element-source.html)

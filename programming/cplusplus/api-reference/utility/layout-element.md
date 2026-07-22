---
layout: default-layout
title: LayoutElement - Dynamsoft Utility C++ Edition API Reference
description: API reference for the LayoutElement structure in Dynamsoft Utility C++ Edition, representing an element in a quadrilateral layout analysis result.
keywords: LayoutElement, layout element, quad, source
needAutoGenerateSidebar: true
---

# LayoutElement

The `LayoutElement` structure represents an element in a layout result. It combines the element's geometry with its origin information.

## Definition

*Assembly:* DynamsoftUtility

*Header File:* DynamsoftUtility.h

```cpp
typedef struct LayoutElement
{
    CQuadrilateral quad;
    LayoutElementSource source;
    char reserved[32];
} LayoutElement;
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`quad`](#quad) | *CQuadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *LayoutElementSource* | Origin of this element (Input / Inferred / None). |

### quad

Geometric coordinates of the element.

```cpp
CQuadrilateral quad;
```

**See Also**

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

### source

Origin of this element.

```cpp
LayoutElementSource source = LES_NONE;
```

**See Also**

[LayoutElementSource]({{ site.dcvb_cpp_api }}utility/enum-layout-element-source.html?lang=cpp)

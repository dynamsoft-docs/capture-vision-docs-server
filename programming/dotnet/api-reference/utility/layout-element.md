---
layout: default-layout
title: LayoutElement Class - Dynamsoft Utility .NET Edition API Reference
description: API reference for the LayoutElement class in Dynamsoft Utility .NET Edition, representing an element in a quadrilateral layout analysis result.
keywords: LayoutElement, layout element, quad, source
needAutoGenerateSidebar: true
---

# LayoutElement

The `LayoutElement` class represents an element in a layout result. It combines the element's geometry with its origin information.

## Definition

*Namespace:* Dynamsoft.Utility

```csharp
public class LayoutElement
```

## Properties

| Property | Type | Description |
|----------|------|-------------|
| [`quad`](#quad) | *Quadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *LayoutElementSource* | Origin of this element (Input / Inferred / None). |

### quad

```csharp
public Quadrilateral quad;
```

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### source

```csharp
public LayoutElementSource source = LayoutElementSource.LES_NONE;
```

**See Also**

[LayoutElementSource]({{ site.dcvb_dotnet_api }}utility/enum-layout-element-source.html)

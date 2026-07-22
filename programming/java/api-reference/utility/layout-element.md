---
layout: default-layout
title: LayoutElement Class - Dynamsoft Utility Java Edition API Reference
description: API reference for the LayoutElement class in Dynamsoft Utility Java Edition, representing an element in a quadrilateral layout analysis result.
keywords: LayoutElement, layout element, quad, source, java
needAutoGenerateSidebar: true
---

# LayoutElement

The `LayoutElement` class represents an element in a layout result. It combines the element's geometry with its origin information.

## Definition

*Package:* `com.dynamsoft.utility`

```java
class LayoutElement
```

## Attributes

| Attribute | Type | Description |
|-----------|------|-------------|
| [`quad`](#quad) | *Quadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *int* | Origin of this element (Input / Inferred / None). |

### quad

```java
public Quadrilateral quad = new Quadrilateral();
```

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### source

```java
public @EnumLayoutElementSource int source = EnumLayoutElementSource.LES_NONE;
```

**See Also**

[EnumLayoutElementSource]({{ site.dcvb_java_api }}utility/enum-layout-element-source.html)

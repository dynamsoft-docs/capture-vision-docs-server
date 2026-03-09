---
layout: default-layout
title: class Edge - Dynamsoft Core Module .NET Edition API Reference
description: API reference for the Edge class in Dynamsoft Core Module .NET Edition, which represents an edge defined by two corner points.
keywords: edge, .NET
needAutoGenerateSidebar: true
---

# Edge

The class `Edge` is a structure composed of two `Corner` points in an image. A `Corner` represents a point at which the image's brightness or color sharply changes. Therefore, an `Edge` is a line segment connecting two such points that have been identified as corners.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
class Edge 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`startCorner`](#startcorner) | *Corner* |
| [`endCorner`](#endcorner) | *Corner* |

### startCorner

The start corner point of the edge.

```csharp
Corner startCorner
```

**See Also**

[Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)

### endCorner

The end corner point of the edge.

```csharp
Corner endCorner
```

**See Also**

[Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)

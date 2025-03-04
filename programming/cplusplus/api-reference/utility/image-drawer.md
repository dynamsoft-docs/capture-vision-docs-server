---
layout: default-layout
title: class CImageDrawer - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageDrawer in Dynamsoft Utility Module.
keywords: image drawer, drawing on image, c++
needAutoGenerateSidebar: true
---

# CImageDrawer

The `CImageDrawer` class is a utility class for drawing various shapes on images.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CImageDrawer
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`DrawOnImage`](#drawonimage) | Draws various shapes on an image. |

### DrawOnImage

Draws various shapes on an image.

```cpp
CImageData *DrawOnImage(const CImageData *pImageData, CQuadrilateral quads[], int quadsCount, int color=0xFFFF0000, int thickness=1);
CImageData *DrawOnImage(const CImageData *pImageData, CLineSegment lines[], int linesCount, int color=0xFFFF0000, int thickness=1);
CImageData *DrawOnImage(const CImageData *pImageData, CContour contours[], int contoursCount, int color=0xFFFF0000, int thickness=1);
CImageData *DrawOnImage(const CImageData *pImageData, CCorner corners[], int cornersCount, int color=0xFFFF0000, int thickness=1);
CImageData *DrawOnImage(const CImageData *pImageData, CEdge edges[], int edgesCount, int color=0xFFFF0000, int thickness=1);
```

**Parameters**

`[in] pImageData` A pointer to the image data to draw on.

`[in] quads[]` An array of quadrilaterals to draw on the image.

`[in] quadsCount` The number of quadrilaterals in the array.

`[in] lines[]` An array of line segments to draw on the image.

`[in] linesCount` The number of line segments in the array.

`[in] contours[]` An array of contours to draw on the image.

`[in] contoursCount` The number of contours in the array.

`[in] corners[]` An array of corners to draw on the image.

`[in] cornersCount` The number of corners in the array.

`[in] edges[]` An array of edges to draw on the image.

`[in] edgesCount` The number of edges in the array.

`[in] color` The color to use for drawing. Defaults to 0xFFFF0000 (red).

`[in] thickness` The thickness of the lines to draw. Defaults to 1.

**Return value**

Returns a pointer to the modified image data.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)

[CLineSegment]({{ site.dcvb_cpp_api }}core/basic-structures/line-segment.html)

[CContour]({{ site.dcvb_cpp_api }}core/basic-structures/contour.html)

[CCorner]({{ site.dcvb_cpp_api }}core/basic-structures/corner.html)

[CEdge]({{ site.dcvb_cpp_api }}core/basic-structures/edge.html)

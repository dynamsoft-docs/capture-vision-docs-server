---
layout: default-layout
title: class ImageDrawer - Dynamsoft Utility Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ImageDrawer in Dynamsoft Utility Module.
keywords: image drawer, drawing on image, .NET
needAutoGenerateSidebar: true
---

# ImageDrawer

The `ImageDrawer` class is a utility class for drawing various shapes on images.

## Definition

*Namespace:* Dynamsoft.Utility


```csharp
class ImageDrawer : IDisposable
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`DrawOnImage`](#drawonimage) | Draws various shapes on an image. |

### DrawOnImage

Draws various shapes on an image.

```csharp
ImageData DrawOnImage(ImageData imageData, Quadrilateral[] quads, int color = unchecked((int)0xFFFF0000), int thickness = 1);
ImageData DrawOnImage(ImageData imageData, LineSegment[] lines, int color = unchecked((int)0xFFFF0000), int thickness = 1);
ImageData DrawOnImage(ImageData imageData, Contour[] contours, int color = unchecked((int)0xFFFF0000), int thickness = 1);
ImageData DrawOnImage(ImageData imageData, Corner[] corners, int color = unchecked((int)0xFFFF0000), int thickness = 1);
ImageData DrawOnImage(ImageData imageData, Edge[] edges, int color = unchecked((int)0xFFFF0000), int thickness = 1);
```

**Parameters**

`[in] imageData` The image data to draw on.

`[in] quads` An array of quadrilaterals to draw on the image.

`[in] lines` An array of line segments to draw on the image.

`[in] contours` An array of contours to draw on the image.

`[in] corners` An array of corners to draw on the image.

`[in] edges` An array of edges to draw on the image.

`[in] color` The color to use for drawing. Defaults to 0xFFFF0000 (red).

`[in] thickness` The thickness of the lines to draw. Defaults to 1.

**Return value**

Returns the modified image data.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

[LineSegment]({{ site.dcvb_dotnet_api }}core/basic-classes/line-segment.html)

[Contour]({{ site.dcvb_dotnet_api }}core/basic-classes/contour.html)

[Corner]({{ site.dcvb_dotnet_api }}core/basic-classes/corner.html)

[Edge]({{ site.dcvb_dotnet_api }}core/basic-classes/edge.html)

---
layout: default-layout
title: class ImageDrawer - Dynamsoft Utility Module Java Edition API Reference
description: This page shows the Java Edition of the class ImageDrawer in Dynamsoft Utility Module.
keywords: image drawer, drawing on image, java
needAutoGenerateSidebar: true
---

# ImageDrawer

The `ImageDrawer` class is a utility class for drawing various shapes on images.

## Definition

*Namespace:* com.dynamsoft.utility

```java
public class ImageDrawer
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`ImageDrawer`](#imagedrawer) | Initializes a new instance of the `ImageDrawer` class. |
| [`drawOnImage`](#drawonimage) | Draws various shapes on an image. |

### ImageDrawer

Initializes a new instance of the `ImageDrawer` class.

```java
ImageDrawer()
```

### drawOnImage

Draws various shapes on an image.

```java
ImageData drawOnImage(ImageData imageData, Quadrilateral[] quads)
ImageData drawOnImage(ImageData imageData, Quadrilateral[] quads, int color, int thickness)
ImageData drawOnImage(ImageData imageData, LineSegment[] lines)
ImageData drawOnImage(ImageData imageData, LineSegment[] lines, int color, int thickness)
ImageData drawOnImage(ImageData imageData, Contour[] contours)
ImageData drawOnImage(ImageData imageData, Contour[] contours, int color, int thickness)
ImageData drawOnImage(ImageData imageData, Corner[] corners)
ImageData drawOnImage(ImageData imageData, Corner[] corners, int color, int thickness)
ImageData drawOnImage(ImageData imageData, Edge[] edges)
ImageData drawOnImage(ImageData imageData, Edge[] edges, int color, int thickness)
```

**Parameters**

`imageData` The image data to draw on.

`quads` The quadrilaterals to draw.

`lines` The line segments to draw.

`contours` The contours to draw.

`corners` The corners to draw.

`edges` The edges to draw.

`color` The color to use for drawing. Defaults to 0 (black).

`thickness` The thickness of the lines to draw. Defaults to 0.

**Return value**

An `ImageData` object representing the modified image data.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

[LineSegment]({{ site.dcvb_java_api }}core/basic-classes/line-segment.html)

[Contour]({{ site.dcvb_java_api }}core/basic-classes/contour.html)

[Corner]({{ site.dcvb_java_api }}core/basic-classes/corner.html)

[Edge]({{ site.dcvb_java_api }}core/basic-classes/edge.html)

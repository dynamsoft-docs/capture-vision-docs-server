---
layout: default-layout
title: class ImageDrawer - Dynamsoft Utility Module Python Edition API Reference
description: This page shows the Python Edition of the class ImageDrawer in Dynamsoft Utility Module.
keywords: image drawer, drawing on image, python
needAutoGenerateSidebar: true
---

# ImageDrawer

The `ImageDrawer` class is a utility class for drawing various shapes on images.

## Definition

*Module:* dynamsoft_utility

```python
class ImageDrawer:
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`draw_on_image`](#draw_on_image) | Draws various shapes on an image. |

### draw_on_image

Draws various shapes on an image.

```python
def draw_on_image(
    self,
    image: ImageData,
    shapes: Union[
        List[Quadrilateral],
        List[LineSegment],
        List[Contour],
        List[Corner],
        List[Edge],
    ],
    color: int = 0xFFFF0000,
    thickness: int = 1,
) -> ImageData:
```

**Parameters**

`image` The image data to draw on.

`shapes` The shapes to draw.

`color` The color to use for drawing. Defaults to 0xFFFF0000 (red).

`thickness` The thickness of the lines to draw. Defaults to 1.

**Return value**

An `ImageData` object representing the modified image data.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

[LineSegment]({{ site.dcvb_python_api }}core/basic-classes/line-segment.html)

[Contour]({{ site.dcvb_python_api }}core/basic-classes/contour.html)

[Corner]({{ site.dcvb_python_api }}core/basic-classes/corner.html)

[Edge]({{ site.dcvb_python_api }}core/basic-classes/edge.html)

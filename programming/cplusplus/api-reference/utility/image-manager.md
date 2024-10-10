---
layout: default-layout
title: class CImageManager - Dynamsoft Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageManager in Dynamsoft Utility Module.
keywords: image manager, drawing on image, c++
needAutoGenerateSidebar: true
---

# CImageManager

The `CImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Namespace:* dynamsoft::utility

*Assembly:* DynamsoftUtility

```cpp
class CImageManager
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`SaveToFile`](#savetofile) | Saves an image to a file. |
| [`DrawOnImage`](#drawonimage) | Draw various shapes on an image. |

### SaveToFile

Saves an image to a file.

```cpp
int SaveToFile(const CImageData *pImageData, const char *path, bool overwrite = true)
```

**Parameters**

`[in] pImageData` A pointer to the image data to be saved.

`[in] path` The targeting file path with the file name and extension name.

`[in] overwrite` A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Return value**

Returns an integer indicating the success of the operation. 0 indicates success, while a non-zero value indicates an error occurred.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)

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

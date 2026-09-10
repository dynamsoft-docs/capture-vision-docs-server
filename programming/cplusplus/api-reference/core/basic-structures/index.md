---
layout: default-layout
title: Basic Structures - Dynamsoft Core C++ Edition API Reference
description: API reference index of the basic structures in the DynamsoftCore module, covering image data, image tags, geometry classes and the image source adapter.
keywords: core, basic structures, c++, api reference
needGenerateH3Content: false
---

# Basic Structures

The following basic structures are defined in the `DynamsoftCore` module:

- [`CCapturedResultBase`](captured-result-base.md): Abstract base class for all captured result collection classes.
- [`CCapturedResultItem`](captured-result-item.md): Abstract base class for all captured result items.
- [`CCoreModule`](core-module.md): Provides module-level utilities such as version retrieval.
- [`CContour`](contour.md): Represents a contour as a set of boundary points.
- [`CCorner`](corner.md): Represents a corner point with its type and intersecting edges.
- [`CEdge`](edge.md): Represents a line segment edge defined by its start and end points.
- [`CFileImageTag`](file-image-tag.md): Tags an image with its source file path and page number.
- [`CImageData`](image-data.md): Encapsulates raw image bytes, width, height, stride, pixel format and orientation.
- [`CImageSourceAdapter`](image-source-adapter.md): Abstract base class for all image source adapters.
- [`CImageSourceErrorListener`](image-source-error-listener.md): Callback interface for receiving errors from image source adapters.
- [`CImageTag`](image-tag.md): Abstract base class for tagging images with source metadata.
- [`CLineSegment`](line-segment.md): Represents a line segment defined by its endpoints.
- [`COriginalImageResultItem`](original-image-result-item.md): Result item containing the original processed image.
- [`CPDFReadingParameter`](pdf-reading-parameter.md): Configures PDF reading mode, DPI and raster data source.
- [`CPoint`](point.md): Represents a 2D coordinate point.
- [`CQuadrilateral`](quadrilateral.md): Represents a four-vertex polygon describing the location of detected objects.
- [`CRawImageResultItem`](raw-image-result-item.md): Result item containing raw image data with its associated tag.
- [`CRect`](rect.md): Represents an axis-aligned rectangle.
- [`CVector4`](vector4.md): Represents a 4-element integer vector used for transform matrix data.
- [`CVideoFrameTag`](video-frame-tag.md): Tags a video frame with its frame ID, quality and timestamp.

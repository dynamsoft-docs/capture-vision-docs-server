---
layout: default-layout
title: Basic Classes - Dynamsoft Core .NET Edition API Reference
description: API reference index of the basic classes in the DynamsoftCore module, covering image data, image tags, geometry classes and the image source adapter.
keywords: core, basic classes, .net, api reference
needGenerateH3Content: false
---

# Basic Classes

The following basic classes are defined in the `DynamsoftCore` module:

- [`CapturedResultBase`](captured-result-base.md): Base class for all captured result types.
- [`CapturedResultItem`](captured-result-item.md): Base class for all types of captured result items.
- [`Contour`](contour.md): Represents a contour composed of a set of points.
- [`CoreModule`](core-module.md): Provides module-level utilities such as version retrieval.
- [`Corner`](corner.md): Represents a corner point formed by two line segments.
- [`Edge`](edge.md): Represents an edge defined by two corner points.
- [`FileImageTag`](file-image-tag.md): Stores image tag information for file-sourced images including file path and page index.
- [`ImageData`](image-data.md): Holds image pixel data along with width, height, stride and pixel format information.
- [`ImageSourceAdapter`](image-source-adapter.md): Abstract base class for providing images to the capture pipeline.
- [`IImageSourceErrorListener`](image-source-error-listener.md): Interface that receives error notifications from the image source.
- [`ImageTag`](image-tag.md): Base class for storing metadata tags associated with images.
- [`LineSegment`](line-segment.md): Represents a line segment defined by two endpoint coordinates.
- [`OriginalImageResultItem`](original-image-result-item.md): Represents the original input image as a captured result item.
- [`PDFReadingParameter`](pdf-reading-parameter.md): Configures PDF reading options such as mode, DPI and raster data source.
- [`Point`](point.md): Represents a 2D point with x and y coordinates.
- [`Quadrilateral`](quadrilateral.md): Represents a quadrilateral shape defined by four corner points.
- [`Rect`](rect.md): Represents a rectangle defined by its top-left point, width and height.
- [`Vector4`](vector4.md): Represents a 4-element vector used for transformation matrices.
- [`VideoFrameTag`](video-frame-tag.md): Stores metadata tags for video frame images including quality and cropping status.

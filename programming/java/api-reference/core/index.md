---
layout: default-layout
title: Core Module API Reference - Dynamsoft Capture Vision Java Edition
description: API reference index of the DynamsoftCore module in Dynamsoft Capture Vision Java Edition, covering basic classes, intermediate results, enumerations, errors and exceptions.
keywords: core, java, api reference
needGenerateH3Content: false
---

# Core Module API Reference - Java Edition

The `DynamsoftCore` module provides the basic data structures, intermediate result units and shared enumerations used across all processing modules.

## Basic Classes

- [Basic Classes Index](basic-classes/index.md): Core data structures such as `ImageData`, `Quadrilateral`, `Point`, and the abstract `ImageSourceAdapter`.

## Intermediate Results

- [Intermediate Results Index](intermediate-results/index.md): Intermediate result units, elements and receivers produced during image processing.

## Enums

- [`BufferOverflowProtectionMode`](enum-buffer-overflow-protection-mode.md): Strategies used when the image source buffer overflows.
- [`CapturedResultItemType`](enum-captured-result-item-type.md): Possible result item types.
- [`ColourChannelUsageType`](enum-colour-channel-usage-type.md): How colour channels are used during image processing.
- [`CornerType`](enum-corner-type.md): How a corner is geometrically formed by its two sides.
- [`CrossVerificationStatus`](enum-cross-verification-status.md): Whether a result has been cross-verified across multiple frames.
- [`ErrorCode`](enum-error-code.md): Error codes returned by Dynamsoft Capture Vision SDK operations.
- [`GrayscaleEnhancementMode`](enum-grayscale-enhancement-mode.md): Enhancement algorithms applied to grayscale images.
- [`GrayscaleTransformationMode`](enum-grayscale-transformation-mode.md): Transformations applied when converting a colour image to grayscale.
- [`ImageCaptureDistanceMode`](enum-image-capture-distance-mode.md): Distinguishes close-up from long-distance image captures.
- [`ImageFileFormat`](enum-image-file-format.md): Supported image file formats.
- [`ImagePixelFormat`](enum-image-pixel-format.md): Supported pixel formats for image data.
- [`ImageTagType`](enum-image-tag-type.md): Distinguishes file-based from video-frame-based image tags.
- [`IntermediateResultUnitType`](enum-intermediate-result-unit-type.md): Types of intermediate result units.
- [`MeasureUnit`](enum-measure-unit.md): How a numeric value is interpreted relative to a reference dimension.
- [`PDFReadingMode`](enum-pdf-reading-mode.md): Modes for reading PDF files.
- [`RasterDataSource`](enum-raster-data-source.md): Whether raster data comes from pages or rendered PDFs.
- [`RegionObjectElementType`](enum-region-object-element-type.md): Types of region object elements.
- [`SectionType`](enum-section-type.md): Processing sections that produce a result.
- [`TransformMatrixType`](enum-transform-matrix-type.md): Transformation matrix types for coordinate conversion.
- [`VideoFrameQuality`](enum-video-frame-quality.md): Quality classification of video frames.

## Errors and Exceptions

- [`CoreError`](core-error.md): Error codes specific to the Core module.
- [`CoreException`](core-exception.md): Exception class providing error code and message for Core module errors.

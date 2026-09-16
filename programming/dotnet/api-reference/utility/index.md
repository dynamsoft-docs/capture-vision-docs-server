---
layout: default-layout
title: Utility Module API Reference - Dynamsoft Capture Vision .NET Edition
description: API reference index of the DynamsoftUtility module in Dynamsoft Capture Vision .NET Edition, covering image source adapters, image utilities, layout analysis and result filtering.
keywords: utility, .net, api reference
needGenerateH3Content: false
---

# Utility Module API Reference - .NET Edition

The `DynamsoftUtility` module provides helper classes for image fetching, image processing, layout analysis and result filtering.

## Image Source Adapters

- [`DirectoryFetcher`](directory-fetcher.md): Loads image files from a specified directory as an image source.
- [`FileFetcher`](file-fetcher.md): Loads image files from specified file paths as an image source.
- [`ProactiveImageSourceAdapter`](proactive-image-source-adapter.md): Actively fetches images at defined intervals for processing.

## Image Utilities

- [`ImageDrawer`](image-drawer.md): Provides methods for drawing overlays and annotations on images.
- [`ImageIO`](image-io.md): Provides methods for reading and saving image files.
- [`ImageProcessor`](image-processor.md): Provides methods for image processing operations.

## Layout Analysis

- [`LayoutAnalyzer`](layout-analyzer.md): Provides high-performance quadrilateral layout analysis.
- [`LayoutAnalysisParameter`](layout-analysis-parameter.md): Input parameters to guide quadrilateral layout analysis.
- [`LayoutAnalysisResult`](layout-analysis-result.md): Comprehensive results of a quadrilateral layout analysis.
- [`LayoutAxis`](layout-axis.md): Configures axis parameters for quadrilateral layout analysis.
- [`LayoutElement`](layout-element.md): Represents an element in a quadrilateral layout analysis result.

## Result Filtering

- [`MultiFrameResultCrossFilter`](multi-frame-result-cross-filter.md): Filters captured results across multiple frames to improve accuracy and reduce duplicates.

## Module and Enums

- [`UtilityModule`](utility-module.md): Provides module-level utilities such as version retrieval.
- [`FilterType`](enum-filter-type.md): Type of image filter applied during image processing operations.
- [`LayoutElementSource`](enum-layout-element-source.md): Origin of an element in layout analysis results.
- [`LayoutPattern`](enum-layout-pattern.md): Strategies for organizing quadrilaterals in layout analysis.

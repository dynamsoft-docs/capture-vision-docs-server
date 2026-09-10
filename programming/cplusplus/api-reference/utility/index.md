---
layout: default-layout
title: Utility Module API Reference - Dynamsoft Capture Vision C++ Edition
description: API reference index of the DynamsoftUtility module in Dynamsoft Capture Vision C++ Edition, covering image source adapters, image utilities, layout analysis and result filtering.
keywords: utility, c++, api reference
needGenerateH3Content: false
---

# Utility Module API Reference - C++ Edition

The `DynamsoftUtility` module provides helper classes for image fetching, image processing, layout analysis and result filtering.

## Image Source Adapters

- [`CDirectoryFetcher`](directory-fetcher.md): Feeds image files from a specified directory into the capture pipeline.
- [`CFileFetcher`](file-fetcher.md): Feeds a single image file into the capture pipeline.
- [`CProactiveImageSourceAdapter`](proactive-image-source-adapter.md): Proactively fetches images from a buffer for continuous processing.

## Image Utilities

- [`CImageDrawer`](image-drawer.md): Draws result overlays (bounding boxes, text) onto images.
- [`CImageIO`](image-io.md): Reads images from files and saves images to files.
- [`CImageProcessor`](image-processor.md): Provides image conversion methods such as grayscale conversion and binarization.

## Layout Analysis

- [`CLayoutAnalyzer`](layout-analyzer.md): Provides high-performance quadrilateral layout analysis.
- [`LayoutAnalysisParameter`](layout-analysis-parameter.md): Input parameters to guide quadrilateral layout analysis.
- [`LayoutAnalysisResult`](layout-analysis-result.md): Comprehensive results of a quadrilateral layout analysis.
- [`LayoutAxis`](layout-axis.md): Configures axis parameters for quadrilateral layout analysis.
- [`LayoutElement`](layout-element.md): Represents an element in a layout analysis result.

## Result Filtering

- [`CMultiFrameResultCrossFilter`](multi-frame-result-cross-filter.md): Filters captured results across multiple frames to improve reliability and reduce duplicates.

## Module and Enums

- [`CUtilityModule`](utility-module.md): Provides module-level utilities such as version retrieval.
- [`FilterType`](enum-filter-type.md): Image filter type applied during image processing operations.
- [`LayoutElementSource`](enum-layout-element-source.md): Origin of an element in layout analysis results.
- [`LayoutPattern`](enum-layout-pattern.md): Strategies for organizing quadrilaterals in layout analysis.

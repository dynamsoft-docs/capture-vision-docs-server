---
layout: default-layout
title: Intermediate Results - Dynamsoft Core C++ Edition API Reference
description: API reference index of the intermediate results in the DynamsoftCore module, covering intermediate result units, elements and receivers.
keywords: core, intermediate results, c++, api reference
needGenerateH3Content: false
---

# Intermediate Results

The following intermediate result classes are defined in the `DynamsoftCore` module:

- [`CAbstractIntermediateResultReceiver`](abstract-intermediate-result-receiver.md): Abstract base class for all intermediate result receivers.
- [`CAuxiliaryRegionElement`](auxiliary-region-element.md): Represents an auxiliary region element for supplementary spatial analysis.
- [`CBinaryImageUnit`](binary-image-unit.md): Unit containing the binarized (black-and-white) image.
- [`CColourImageUnit`](colour-image-unit.md): Unit containing the colour image at a specific pipeline stage.
- [`CContoursUnit`](contours-unit.md): Unit containing contours and hierarchy data of detected regions.
- [`CEnhancedGrayscaleImageUnit`](enhanced-grayscale-image-unit.md): Unit containing the grayscale image after enhancement.
- [`CGrayscaleImageUnit`](grayscale-image-unit.md): Unit containing the grayscale-converted image.
- [`CIntermediateResult`](intermediate-result.md): Collection of intermediate result units from a single processing step.
- [`CIntermediateResultUnit`](intermediate-result-unit.md): Abstract base class for all intermediate result units.
- [`CLineSegmentsUnit`](line-segments-unit.md): Unit holding all detected line segments.
- [`CObservationParameters`](observed-parameters.md): Specifies which intermediate result unit types and sections to observe.
- [`CPredetectedRegionElement`](predetected-region-element.md): Represents a pre-detected region of interest.
- [`CPredetectedRegionsUnit`](predetected-regions-unit.md): Unit holding all pre-detected regions.
- [`CRegionObjectElement`](region-object-element.md): Abstract base class for region-based result elements.
- [`CScaledColourImageUnit`](scaled-colour-image-unit.md): Unit containing the colour image after scaling.
- [`CScaledDownColourImageUnit`](scaled-down-colour-image-unit.md): Unit containing the colour image after downscaling.
- [`CShortLinesUnit`](short-lines-unit.md): Unit containing detected short line segments.
- [`CTextRemovedBinaryImageUnit`](text-removed-binary-image-unit.md): Unit containing the binary image with text regions removed.
- [`CTextZone`](text-zone.md): Represents a single detected text zone.
- [`CTextZonesUnit`](text-zones-unit.md): Unit holding detected text zones.
- [`CTextureDetectionResultUnit`](texture-detection-result-unit.md): Unit containing detected texture patterns.
- [`CTextureRemovedBinaryImageUnit`](texture-removed-binary-image-unit.md): Unit containing the binary image with background texture removed.
- [`CTextureRemovedGrayscaleImageUnit`](texture-removed-grayscale-image-unit.md): Unit containing the grayscale image with background texture removed.
- [`CTransformedGrayscaleImageUnit`](transformed-grayscale-image-unit.md): Unit containing the grayscale image after transformation.

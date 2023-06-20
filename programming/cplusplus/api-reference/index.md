---
layout: default-layout
title: Index - Dynamsoft Capture Vision C++ Edition API Reference
description: The index of Dynamsoft Capture Vision C++ edition API reference.
keywords: API reference, index, c++
needAutoGenerateSidebar: true
---

# Dynamsoft Capture Vision API Reference - C++ Edition

## Primary Class

- [`CCaptureVisionRouter`]({{ site.cpp_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.cpp_api }}utility/directory-fetcher.html)
- [`CImageSourceAdapter`]({{ site.cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.cpp_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.cpp_api }}core/basic-structures/captured-result-receiver.html)
- [`CCapturedResult`]({{ site.cpp_api }}core/basic-structures/captured-result.html)
- [`CCapturedResultArray`]({{ site.cpp_api }}core/basic-structures/captured-result-array.html)
- [`CCapturedResultItem`]({{ site.cpp_api }}core/basic-structures/captured-result-item.html)
- [`CBarcodeResultItem`]({{ site.dbr_cpp_api }}barcode-result-item.html)
- [`CDecodedBarcodesResult`]({{ site.dbr_cpp_api }}decoded-barcodes-result.html)
- [`CDecodedBarcodesResultArray`]({{ site.dbr_cpp_api }}decoded-barcodes-result-array.html)
- [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html)
- [`CCharacterResult`]({{ site.dlr_cpp_api }}character-result.html)
- [`CRecognizedTextLinesResult`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html)
- [`CDetectedQuadResultItem`]({{ site.ddn_cpp_api }}detected-quad-result-item.html)
- [`CDetectedQuadsResult`]({{ site.ddn_cpp_api }}detected-quads-result.html)
- [`CDetectedQuadsResultArray`]({{ site.ddn_cpp_api }}detected-quads-result-array.html)
- [`CNormalizedImageResultItem`]({{ site.ddn_cpp_api }}normalized-image-result-item.html)
- [`CNormalizedImagesResult`]({{ site.ddn_cpp_api }}normalized-images-result.html)
- [`CNormalizedImagesResultArray`]({{ site.ddn_cpp_api }}normalized-images-result-array.html)
- [`CParsedResultItem`]({{ site.dcp_cpp_api }}parsed-result-item.html)
- [`CParsedResult`]({{ site.dcp_cpp_api }}parsed-result.html)
- [`CRawImageResultItem`]({{ site.cpp_api }}core/basic-structures/raw-image-result-item.html)

## Final Results Filters

- [`CCapturedResultFilter`]({{ site.cpp_api }}core/basic-structures/captured-result-filter.html)
- [`CMultiFrameResultCrossFilter`]({{ site.cpp_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`CIntermediateResultManager`]({{ site.cpp_api }}core/intermediate-results/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.cpp_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CObservationParameters`]({{ site.cpp_api }}core/intermediate-results/observed-parameters.html)
- [`IntermediateResultExtraInfo`]({{ site.cpp_api }}core/structs/intermediate-result-extra-info.html)
- [`CIntermediateResult`]({{ site.cpp_api }}core/intermediate-results/intermediate-result.html)
- [`CIntermediateResultUnit`]({{ site.cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CPredetectedRegionsUnit`]({{ site.cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CBinaryImageUnit`]({{ site.cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CColourImageUnit`]({{ site.cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CContoursUnit`]({{ site.cpp_api }}core/intermediate-results/contours-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CLineSegmentsUnit`]({{ site.cpp_api }}core/intermediate-results/line-segments-unit.html)
- [`CScaledDownColourImageUnit`]({{ site.cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextRemovedBinaryImageUnit`]({{ site.cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`CTextZonesUnit`]({{ site.cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
- [`CScaledUpBarcodeImageUnit`]({{ site.dbr_cpp_api }}scaled-up-barcode-image-unit.html)
- [`CCandidateBarcodeZonesUnit`]({{ site.dbr_cpp_api }}candidate-barcode-zones-unit.html)
- [`CComplementedBarcodeImageUnit`]({{ site.dbr_cpp_api }}complemented-barcode-image-unit.html)
- [`CDeformationResistedBarcodeImageUnit`]({{ site.dbr_cpp_api }}deformation-resisted-barcode-image-unit.html)
- [`CLocalizedBarcodesUnit`]({{ site.dbr_cpp_api }}localized-barcodes-unit.html)
- [`CDecodedBarcodesUnit`]({{ site.dbr_cpp_api }}decoded-barcodes-unit.html)
- [`CLocalizedTextLinesUnit`]({{ site.dlr_cpp_api }}localized-text-lines-unit.html)
- [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html)
- [`CLongLinesUnit`]({{ site.ddn_cpp_api }}long-lines-unit.html)
- [`CCornersUnit`]({{ site.ddn_cpp_api }}corners-unit.html)
- [`CCandidateQuadEdgesUnit`]({{ site.ddn_cpp_api }}candidate-quad-edges-unit.html)
- [`CDetectedQuadsUnit`]({{ site.ddn_cpp_api }}detected-quads-unit.html)
- [`CNormalizedImagesUnit`]({{ site.ddn_cpp_api }}normalized-image-unit.html)
- [`CRegionObjectElement`]({{ site.cpp_api }}core/intermediate-results/region-object-element.html)
- [`CPredetectedRegionElement`]({{ site.cpp_api }}core/intermediate-results/predetected-region-element.html)
- [`CLocalizedBarcodesElement`]({{ site.dbr_cpp_api }}localized-barcode-element.html)
- [`CDecodedBarcodeElement`]({{ site.dbr_cpp_api }}decoded-barcode-element.html)
- [`CLocalizedTextLineElement`]({{ site.dlr_cpp_api }}localized-text-line-element.html)
- [`CRecognizedTextLineElement`]({{ site.dlr_cpp_api }}recognized-text-line-element.html)
- [`CDetectedQuadElement`]({{ site.ddn_cpp_api }}detected-quad-element.html)
- [`CNormalizedImageElement`]({{ site.ddn_cpp_api }}normalized-image-element.html)
- [`CExtendedBarcodeResult`]({{ site.dbr_cpp_api }}extended-barcode-result.html)

## Detailed Barcode Results

- [`CAztecDetails`]({{ site.dbr_cpp_api }}aztec-details.html)
- [`CBarcodeDetails`]({{ site.dbr_cpp_api }}barcode-details.html)
- [`CDataMatrixDetails`]({{ site.dbr_cpp_api }}datamatrix-details.html)
- [`COneDCodeDetails`]({{ site.dbr_cpp_api }}oned-code-details.html)
- [`CPDF417Details`]({{ site.dbr_cpp_api }}pdf417-details.html)
- [`CQRCodeDetails`]({{ site.dbr_cpp_api }}qr-code-details.html)

## Settings

- [`SimplifiedCaptureVisionSettings`]({{ site.cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_cpp_api }}simplified-barcode-reader-settings.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_cpp_api }}simplified-label-recognizer-settings.html)
- [`CPresetTemplate`]({{ site.cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html)

## State Listener

- [`CCaptureStateListener`]({{ site.cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CImageSourceStateListener`]({{ site.cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## [`CLicenseManager`]({{ site.cpp_api }}license/license-manager.html)

## Basic Structure

- [`CContour`]({{ site.cpp_api }}core/basic-structures/contour.html)
- [`CCorner`]({{ site.cpp_api }}core/basic-structures/corner.html)
- [`CEdge`]({{ site.cpp_api }}core/basic-structures/edge.html)
- [`CFileImageTag`]({{ site.cpp_api }}core/basic-structures/file-image-tag.html)
- [`CImageData`]({{ site.cpp_api }}core/basic-structures/image-data.html)
- [`CImageTag`]({{ site.cpp_api }}core/basic-structures/image-tag.html)
- [`CLineSegment`]({{ site.cpp_api }}core/basic-structures/line-segment.html)
- [`CPDFReadingParameter`]({{ site.cpp_api }}core/basic-structures/pdf-reading-parameter.html)
- [`CPoint`]({{ site.cpp_api }}core/basic-structures/point.html)
- [`CQuadrilateral`]({{ site.cpp_api }}core/basic-structures/quadrilateral.html)
- [`CRect`]({{ site.cpp_api }}core/basic-structures/rect.html)
- [`CVideoFrameTag`]({{ site.cpp_api }}core/basic-structures/video-frame-tag.html)

## Modules

- [`CCaptureVisionRouterModule`]({{ site.cpp_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CBarcodeReaderModule`]({{ site.dbr_cpp_api }}barcode-reader-module.html)
- [`CLabelRecognizerModule`]({{ site.dlr_cpp_api }}label-recognizer-module.html)
- [`CDocumentNormalizerModule`]({{ site.ddn_cpp_api }}document-normalizer-module.html)
- [`CCoreModule`]({{ site.cpp_api }}core/basic-structures/core-module.html)
- [`CLicenseModule`]({{ site.cpp_api }}license/license-module.html)
- [`CUtilityModule`]({{ site.cpp_api }}utility/utility-module.html)
- [`CImageProcessingModule`]({{ site.cpp_api }}image-processing/image-processing-module.html)

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.enumerations }}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)
- [`CapturedResultItemType`]({{ site.enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)
- [`CornerType`]({{ site.enumerations }}core/corner-type.html?src=cpp&&lang=cpp)
- [`ErrorCode`]({{ site.enumerations }}core/error-code.html?src=cpp&&lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.enumerations }}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.enumerations }}core/image-capture-distance-mode.html?src=cpp&&lang=cpp)
- [`ImagePixelFormat`]({{ site.enumerations }}core/image-pixel-format.html?src=cpp&&lang=cpp)
- [`ImageSourceState`]({{ site.enumerations }}core/image-source-state.html?src=cpp&&lang=cpp)
- [`ImageTagType`]({{ site.enumerations }}core/image-tag-type.html?src=cpp&&lang=cpp)
- [`IntermediateResultUnitType`]({{ site.enumerations }}core/intermediate-result-unit-type.html?src=cpp&&lang=cpp)
- [`PDFReadingMode`]({{ site.enumerations }}core/pdf-reading-mode.html?src=cpp&&lang=cpp)
- [`RegionObjectElementType`]({{ site.enumerations }}core/region-object-element-type.html?src=cpp&&lang=cpp)
- [`SectionType`]({{ site.enumerations }}core/section-type.html?src=cpp&&lang=cpp)
- [`TargetType`]({{ site.enumerations }}core/target-type.html?src=cpp&&lang=cpp)
- [`VideoFrameQuality`]({{ site.enumerations }}core/video-frame-quality.html?src=cpp&&lang=cpp)
- [`ColourChannelUsageType`]({{ site.enumerations}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)

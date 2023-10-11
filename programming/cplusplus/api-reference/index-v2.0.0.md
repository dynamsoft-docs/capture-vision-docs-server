---
layout: default-layout
title: Index - Dynamsoft Capture Vision C++ Edition API Reference
description: The index of Dynamsoft Capture Vision C++ edition API reference.
keywords: API reference, index, c++
needAutoGenerateSidebar: true
---

# Dynamsoft Capture Vision API Reference - C++ Edition

## Primary Class

- [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)
- [`CFileFetcher`]({{ site.dcv_cpp_api }}utility/file-fetcher.html)
- [`CImageSourceAdapter`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_cpp_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-receiver.html)
- [`CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html)
- [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)
- [`CBarcodeResultItem`]({{ site.dbr_cpp_api }}barcode-result-item.html)
- [`CDecodedBarcodesResult`]({{ site.dbr_cpp_api }}decoded-barcodes-result.html)
- [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html)
- [`CCharacterResult`]({{ site.dlr_cpp_api }}character-result.html)
- [`CRecognizedTextLinesResult`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html)
- [`CDetectedQuadResultItem`]({{ site.ddn_cpp_api }}detected-quad-result-item.html)
- [`CDetectedQuadsResult`]({{ site.ddn_cpp_api }}detected-quads-result.html)
- [`CNormalizedImageResultItem`]({{ site.ddn_cpp_api }}normalized-image-result-item.html)
- [`CNormalizedImagesResult`]({{ site.ddn_cpp_api }}normalized-images-result.html)
- [`CParsedResultItem`]({{ site.dcp_cpp_api }}parsed-result-item.html)
- [`CParsedResult`]({{ site.dcp_cpp_api }}parsed-result.html)
- [`CRawImageResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/raw-image-result-item.html)

## Final Results Filters

- [`CCapturedResultFilter`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-filter.html)
- [`CMultiFrameResultCrossFilter`]({{ site.dcv_cpp_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`CIntermediateResultManager`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CObservationParameters`]({{ site.dcv_cpp_api }}core/intermediate-results/observed-parameters.html)
- [`IntermediateResultExtraInfo`]({{ site.dcv_cpp_api }}core/structs/intermediate-result-extra-info.html)
- [`CIntermediateResult`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result.html)
- [`CIntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CLocalizedBarcodesUnit`]({{ site.dbr_cpp_api }}localized-barcodes-unit.html)
- [`CDecodedBarcodesUnit`]({{ site.dbr_cpp_api }}decoded-barcodes-unit.html)
- [`CLocalizedTextLinesUnit`]({{ site.dlr_cpp_api }}localized-text-lines-unit.html)
- [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html)
- [`CDetectedQuadsUnit`]({{ site.ddn_cpp_api }}detected-quads-unit.html)
- [`CNormalizedImagesUnit`]({{ site.ddn_cpp_api }}normalized-image-unit.html)
- [`CRegionObjectElement`]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html)
- [`CPredetectedRegionElement`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)
- [`CLocalizedBarcodesElement`]({{ site.dbr_cpp_api }}localized-barcode-element.html)
- [`CDecodedBarcodeElement`]({{ site.dbr_cpp_api }}decoded-barcode-element.html)
- [`CLocalizedTextLineElement`]({{ site.dlr_cpp_api }}localized-text-line-element.html)
- [`CRecognizedTextLineElement`]({{ site.dlr_cpp_api }}recognized-text-line-element.html)
- [`CDetectedQuadElement`]({{ site.ddn_cpp_api }}detected-quad-element.html)
- [`CNormalizedImageElement`]({{ site.ddn_cpp_api }}normalized-image-element.html)
- [`CExtendedBarcodeResult`]({{ site.dbr_cpp_api }}extended-barcode-result.html)
- [`CBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CContoursUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/contours-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CLineSegmentsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/line-segments-unit.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`CTextZonesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
- [`CScaledUpBarcodeImageUnit`]({{ site.dbr_cpp_api }}scaled-up-barcode-image-unit.html)
- [`CCandidateBarcodeZonesUnit`]({{ site.dbr_cpp_api }}candidate-barcode-zones-unit.html)
- [`CComplementedBarcodeImageUnit`]({{ site.dbr_cpp_api }}complemented-barcode-image-unit.html)
- [`CDeformationResistedBarcodeImageUnit`]({{ site.dbr_cpp_api }}deformation-resisted-barcode-image-unit.html)
- [`CLongLinesUnit`]({{ site.ddn_cpp_api }}long-lines-unit.html)
- [`CCornersUnit`]({{ site.ddn_cpp_api }}corners-unit.html)
- [`CCandidateQuadEdgesUnit`]({{ site.ddn_cpp_api }}candidate-quad-edges-unit.html)

## Detailed Barcode Results

- [`CAztecDetails`]({{ site.dbr_cpp_api }}aztec-details.html)
- [`CBarcodeDetails`]({{ site.dbr_cpp_api }}barcode-details.html)
- [`CDataMatrixDetails`]({{ site.dbr_cpp_api }}datamatrix-details.html)
- [`COneDCodeDetails`]({{ site.dbr_cpp_api }}oned-code-details.html)
- [`CPDF417Details`]({{ site.dbr_cpp_api }}pdf417-details.html)
- [`CQRCodeDetails`]({{ site.dbr_cpp_api }}qr-code-details.html)

## Settings

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_cpp_api }}simplified-barcode-reader-settings.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_cpp_api }}simplified-label-recognizer-settings.html)
- [`CPresetTemplate`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html)

## State Listener

- [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## License

- [`CLicenseManager`]({{ site.dcv_cpp_api }}license/license-manager.html)

## Basic Structure

- [`CContour`]({{ site.dcv_cpp_api }}core/basic-structures/contour.html)
- [`CCorner`]({{ site.dcv_cpp_api }}core/basic-structures/corner.html)
- [`CEdge`]({{ site.dcv_cpp_api }}core/basic-structures/edge.html)
- [`CFileImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/file-image-tag.html)
- [`CImageData`]({{ site.dcv_cpp_api }}core/basic-structures/image-data.html)
- [`CImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/image-tag.html)
- [`CLineSegment`]({{ site.dcv_cpp_api }}core/basic-structures/line-segment.html)
- [`CPDFReadingParameter`]({{ site.dcv_cpp_api }}core/basic-structures/pdf-reading-parameter.html)
- [`CPoint`]({{ site.dcv_cpp_api }}core/basic-structures/point.html)
- [`CQuadrilateral`]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)
- [`CRect`]({{ site.dcv_cpp_api }}core/basic-structures/rect.html)
- [`CVideoFrameTag`]({{ site.dcv_cpp_api }}core/basic-structures/video-frame-tag.html)

## Modules

- [`CCaptureVisionRouterModule`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CBarcodeReaderModule`]({{ site.dbr_cpp_api }}barcode-reader-module.html)
- [`CLabelRecognizerModule`]({{ site.dlr_cpp_api }}label-recognizer-module.html)
- [`CDocumentNormalizerModule`]({{ site.ddn_cpp_api }}document-normalizer-module.html)
- [`CCoreModule`]({{ site.dcv_cpp_api }}core/basic-structures/core-module.html)
- [`CLicenseModule`]({{ site.dcv_cpp_api }}license/license-module.html)
- [`CUtilityModule`]({{ site.dcv_cpp_api }}utility/utility-module.html)
- [`CImageProcessingModule`]({{ site.dcv_cpp_api }}image-processing/image-processing-module.html)

## Enumerations

- [`BarcodeFormat`]({{ site.enums }}barcode-reader/barcode-format.html?src=cpp&&lang=cpp)
- [`BufferOverflowProtectionMode`]({{ site.enums }}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)
- [`CapturedResultItemType`]({{ site.enums }}core/captured-result-item-type.html?src=cpp&&lang=cpp)
- [`CaptureState`]({{ site.enums }}capture-vision-router/capture-state.html?src=cpp&&lang=cpp)
- [`CornerType`]({{ site.enums }}core/corner-type.html?src=cpp&&lang=cpp)
- [`DeblurMode`]({{ site.enums }}barcode-reader/deblur-mode.html?src=cpp&&lang=cpp)
- [`ErrorCode`]({{ site.enums }}core/error-code.html?src=cpp&&lang=cpp)
- [`ExtendedBarcodeResultType`]({{ site.enums }}barcode-reader/extended-barcode-result-type.html?src=cpp&&lang=cpp)
- [`GrayscaleEnhancementMode`]({{ site.enums }}core/grayscale-enhancement-mode.html?src=cpp&&lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.enums }}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.enums }}core/image-capture-distance-mode.html?src=cpp&&lang=cpp)
- [`ImagePixelFormat`]({{ site.enums }}core/image-pixel-format.html?src=cpp&&lang=cpp)
- [`ImageSourceState`]({{ site.enums }}core/image-source-state.html?src=cpp&&lang=cpp)
- [`ImageTagType`]({{ site.enums }}core/image-tag-type.html?src=cpp&&lang=cpp)
- [`IntermediateResultUnitType`]({{ site.enums }}core/intermediate-result-unit-type.html?src=cpp&&lang=cpp)
- [`LocalizationMode`]({{ site.enums }}barcode-reader/localization-mode.html?src=cpp&&lang=cpp)
- [`MappingStatus`]({{ site.enums }}code-parser/mapping-status.html?src=cpp&&lang=cpp)
- [`PDFReadingMode`]({{ site.enums }}core/pdf-reading-mode.html?src=cpp&&lang=cpp)
- [`QRCodeErrorCorrectionLevel`]({{ site.enums }}barcode-reader/qr-code-error-correction-level.html?src=cpp&&lang=cpp)
- [`RegionObjectElementType`]({{ site.enums }}core/region-object-element-type.html?src=cpp&&lang=cpp)
- [`SectionType`]({{ site.enums }}core/section-type.html?src=cpp&&lang=cpp)
- [`TargetType`]({{ site.enums }}core/target-type.html?src=cpp&&lang=cpp)
- [`ValiadtionStatus`]({{ site.enums }}code-parser/validation-status.html?src=cpp&&lang=cpp)
- [`VideoFrameQuality`]({{ site.enums }}core/video-frame-quality.html?src=cpp&&lang=cpp)
- [`ColourChannelUsageType`]({{ site.enums}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)

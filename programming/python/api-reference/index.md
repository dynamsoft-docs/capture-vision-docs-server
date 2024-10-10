---
layout: default-layout
title: Index - Dynamsoft Capture Vision Module Python Edition API Reference
description: The index of Dynamsoft Capture Vision Python Edition API reference.
keywords: API reference, index, python
needAutoGenerateSidebar: false
---

# Dynamsoft Capture Vision API Reference - Python Edition

## DynamsoftCaptureVisionRouter

### [CaptureVisionRouter]({{ site.dcvb_python_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor`]({{ site.dcvb_python_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcvb_python_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcvb_python_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcvb_python_api }}capture-vision-router/settings.html)
- [`Buffered Items`]({{ site.dcvb_python_api }}capture-vision-router/buffered-items.html)

### Classes

- [`BufferedItemsManager`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/buffered-items-manager.html)
- [`CaptureStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CaptureVisionRouterModule`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CapturedResultFilter`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CapturedResultReceiver`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`CapturedResult`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)
- [`ImageSourceStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`SimplifiedCaptureVisionSettings`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

### Enums

- [`EnumCaptureState`]({{ site.dcvb_enumerations }}capture-vision-router/capture-state.html?lang=python)
- [`EnumImageSourceState`]({{ site.dcvb_enumerations }}capture-vision-router/image-source-state.html?lang=python)
- [`EnumPresetTemplate`]({{ site.dcvb_enumerations }}capture-vision-router/preset-template.html?lang=python)

## DynamsoftBarcodeReader

### Classes

- [`AztecDetails`]({{ site.dbr_python_api }}aztec-details.html)
- [`BarcodeDetails`]({{ site.dbr_python_api }}barcode-details.html)
- [`BarcodeReaderModule`]({{ site.dbr_python_api }}barcode-reader-module.html)
- [`BarcodeResultItem`]({{ site.dbr_python_api }}barcode-result-item.html)
- [`DataMatrixDetails`]({{ site.dbr_python_api }}datamatrix-details.html)
- [`DecodedBarcodesResult`]({{ site.dbr_python_api }}decoded-barcodes-result.html)
- [`OneDCodeDetails`]({{ site.dbr_python_api }}oned-code-details.html)
- [`PDF417Details`]({{ site.dbr_python_api }}pdf417-details.html)
- [`QRCodeDetails`]({{ site.dbr_python_api }}qr-code-details.html)
- [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_python_api }}simplified-barcode-reader-settings.html)

### Enums

- [`EnumBarcodeFormat`]({{ site.dcvb_enumerations }}barcode-reader/barcode-format.html?lang=python)
- [`EnumDeblurMode`]({{ site.dcvb_enumerations }}barcode-reader/deblur-mode.html?lang=python)
- [`EnumExtendedBarcodeResultType`]({{ site.dcvb_enumerations }}barcode-reader/extended-barcode-result-type.html?lang=python)
- [`EnumLocalizationMode`]({{ site.dcvb_enumerations }}barcode-reader/localization-mode.html?lang=python)
- [`EnumQRCodeErrorCorrectionLevel`]({{ site.dcvb_enumerations }}barcode-reader/qr-code-error-correction-level.html?lang=python)

## DynamsoftLabelRecognizer

### Classes

- [`BufferedCharacterItemSet`]({{ site.dlr_python_api }}buffered-character-item-set.html)
- [`BufferedCharacterItem`]({{ site.dlr_python_api }}buffered-character-item.html)
- [`CharacterCluster`]({{ site.dlr_python_api }}character-cluster.html)
- [`CharacterResult`]({{ site.dlr_python_api }}character-result.html)
- [`LabelRecognizerModule`]({{ site.dlr_python_api }}label-recognizer-module.html)
- [`RecognizedTextLinesResult`]({{ site.dlr_python_api }}recognized-text-lines-result.html)
- [`TextLineResultItem`]({{ site.dlr_python_api }}text-line-result-item.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_python_api }}simplified-label-recognizer-settings.html)

## DynamsoftDocumentNormalizer

### Classes

- [`DetectedQuadResultItem`]({{ site.ddn_python_api }}detected-quad-result-item.html)
- [`DetectedQuadsResult`]({{ site.ddn_python_api }}detected-quads-result.html)
- [`DocumentNormalizerModule`]({{ site.ddn_python_api }}document-normalizer-module.html)
- [`NormalizedImageResultItem`]({{ site.ddn_python_api }}normalized-image-result-item.html)
- [`NormalizedImagesResult`]({{ site.ddn_python_api }}normalized-images-result.html)
- [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_python_api }}simplified-document-normalizer-settings.html)

### Enums

- [`EnumImageColourMode`]({{ site.dcvb_enumerations }}document-normalizer/image-colour-mode.html?lang=python)

## DynamsoftCodeParser

### Classes

- [`CodeParserModule`]({{ site.dcp_python_api }}code-parser-module.html)
- [`ParsedResultItem`]({{ site.dcp_python_api }}parsed-result-item.html)
- [`ParsedResult`]({{ site.dcp_python_api }}parsed-result.html)

### Enums

- [`EnumMappingStatus`]({{ site.dcvb_enumerations }}code-parser/mapping-status.html?lang=python)
- [`EnumValiadtionStatus`]({{ site.dcvb_enumerations }}code-parser/validation-status.html?lang=python)

## DynamsoftCore

### Classes

- [`CapturedResultItem`]({{ site.dcvb_python_api }}core/basic-classes/captured-result-item.html)
- [`CoreModule`]({{ site.dcvb_python_api }}core/basic-classes/core-module.html)
- [`FileImageTag`]({{ site.dcvb_python_api }}core/basic-classes/file-image-tag.html)
- [`ImageData`]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)
- [`ImageSourceAdapter`]({{ site.dcvb_python_api }}core/basic-classes/image-source-adapter.html)
- [`ImageSourceErrorListener`]({{ site.dcvb_python_api }}core/basic-classes/image-source-error-listener.html)
- [`ImageTag`]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)
- [`OriginalImageResultItem`]({{ site.dcvb_python_api }}core/basic-classes/original-image-result-item.html)
- [`PDFReadingParameter`]({{ site.dcvb_python_api }}core/basic-classes/pdf-reading-parameter.html)
- [`Point`]({{ site.dcvb_python_api }}core/basic-classes/point.html)
- [`Quadrilateral`]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)
- [`Rect`]({{ site.dcvb_python_api }}core/basic-classes/rect.html)
- [`VideoFrameTag`]({{ site.dcvb_python_api }}core/basic-classes/video-frame-tag.html)

### Enums

- [`EnumBufferOverflowProtectionMode`]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=python)
- [`EnumCapturedResultItemType`]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=python)
- [`EnumColourChannelUsageType`]({{ site.dcvb_enumerations }}core/colour-channel-usage-type.html?lang=python)
- [`EnumErrorCode`]({{ site.dcvb_enumerations }}core/error-code.html?lang=python)
- [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_enumerations }}core/grayscale-enhancement-mode.html?lang=python)
- [`EnumGrayscaleTransformationMode`]({{ site.dcvb_enumerations }}core/grayscale-transformation-mode.html?lang=python)
- [`EnumImageCaptureDistanceMode`]({{ site.dcvb_enumerations }}core/image-capture-distance-mode.html?lang=python)
- [`EnumImagePixelFormat`]({{ site.dcvb_enumerations }}core/image-pixel-format.html?lang=python)
- [`EnumImageTagType`]({{ site.dcvb_enumerations }}core/image-tag-type.html?lang=python)
- [`EnumPDFReadingMode`]({{ site.dcvb_enumerations }}core/pdf-reading-mode.html?lang=python)                
- [`EnumRasterDataSource`]({{ site.dcvb_enumerations }}core/raster-data-source.html?lang=python)
- [`EnumVideoFrameQuality`]({{ site.dcvb_enumerations }}core/video-frame-quality.html?lang=python)

## DynamsoftUtility

- [`DirectoryFetcher`]({{ site.dcvb_python_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcvb_python_api }}utility/file-fetcher.html)
- [`ImageManager`]({{ site.dcvb_python_api }}utility/image-manager.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcvb_python_api }}utility/multi-frame-result-cross-filter.html)
- [`ProactiveImageSourceAdapter`]({{ site.dcvb_python_api }}utility/proactive-image-source-adapter.html)
- [`UtilityModule`]({{ site.dcvb_python_api }}utility/utility-module.html)

## DynamsoftLicense

- [`LicenseManager`]({{ site.dcvb_python_api }}license/license-manager.html)
- [`LicenseModule`]({{ site.dcvb_python_api }}license/license-module.html)


## DynamsoftImageProcessing

- [`ImageProcessingModule`]({{ site.dcvb_python_api }}image-processing/image-processing-module.html)


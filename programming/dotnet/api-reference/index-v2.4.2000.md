---
layout: default-layout
title: Index - Dynamsoft Capture Vision Module .NET Edition API Reference
description: The index of Dynamsoft Capture Vision .NET Edition API reference.
keywords: API reference, index, .NET
needAutoGenerateSidebar: false
---

# Dynamsoft Capture Vision API Reference - .NET Edition

## DynamsoftCaptureVisionRouter

### [CaptureVisionRouter]({{ site.dcvb_dotnet_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor and Destructor`]({{ site.dcvb_dotnet_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcvb_dotnet_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcvb_dotnet_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html)

### Classes

- [`ICaptureStateListener`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CaptureVisionRouterModule`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CapturedResult`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result.html)
- [`CapturedResultFilter`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CapturedResultReceiver`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`IImageSourceStateListener`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`PresetTemplate`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html)

### Structs

- [`SimplifiedCaptureVisionSettings`]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

### Enums

- [`EnumCaptureState`]({{ site.dcvb_enumerations }}capture-vision-router/capture-state.html?lang=dotnet)
- [`EnumImageSourceState`]({{ site.dcvb_enumerations }}capture-vision-router/image-source-state.html?lang=dotnet)

## DynamsoftBarcodeReader

### Classes

- [`AztecDetails`]({{ site.dbr_dotnet_api }}aztec-details.html)
- [`BarcodeDetails`]({{ site.dbr_dotnet_api }}barcode-details.html)
- [`BarcodeReaderModule`]({{ site.dbr_dotnet_api }}barcode-reader-module.html)
- [`BarcodeResultItem`]({{ site.dbr_dotnet_api }}barcode-result-item.html)
- [`DataMatrixDetails`]({{ site.dbr_dotnet_api }}datamatrix-details.html)
- [`DecodedBarcodesResult`]({{ site.dbr_dotnet_api }}decoded-barcodes-result.html)
- [`OneDCodeDetails`]({{ site.dbr_dotnet_api }}oned-code-details.html)
- [`PDF417Details`]({{ site.dbr_dotnet_api }}pdf417-details.html)
- [`QRCodeDetails`]({{ site.dbr_dotnet_api }}qr-code-details.html)

### Structs

- [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_dotnet_api }}simplified-barcode-reader-settings.html)

### Enums

- [`EnumBarcodeFormat`]({{ site.dcvb_enumerations }}barcode-reader/barcode-format.html?lang=dotnet)
- [`EnumDeblurMode`]({{ site.dcvb_enumerations }}barcode-reader/deblur-mode.html?lang=dotnet)
- [`EnumExtendedBarcodeResultType`]({{ site.dcvb_enumerations }}barcode-reader/extended-barcode-result-type.html?lang=dotnet)
- [`EnumLocalizationMode`]({{ site.dcvb_enumerations }}barcode-reader/localization-mode.html?lang=dotnet)
- [`EnumQRCodeErrorCorrectionLevel`]({{ site.dcvb_enumerations }}barcode-reader/qr-code-error-correction-level.html?lang=dotnet)

## DynamsoftLabelRecognizer

### Classes

- [`CharacterResult`]({{ site.dlr_dotnet_api }}character-result.html)
- [`LabelRecognizerModule`]({{ site.dlr_dotnet_api }}label-recognizer-module.html)
- [`RecognizedTextLinesResult`]({{ site.dlr_dotnet_api }}recognized-text-lines-result.html)
- [`TextLineResultItem`]({{ site.dlr_dotnet_api }}text-line-result-item.html)

### Structs

- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_dotnet_api }}simplified-label-recognizer-settings.html)

## DynamsoftDocumentNormalizer

### Classes

- [`DetectedQuadResultItem`]({{ site.ddn_dotnet_api }}detected-quad-result-item.html)
- [`DetectedQuadsResult`]({{ site.ddn_dotnet_api }}detected-quads-result.html)
- [`DocumentNormalizerModule`]({{ site.ddn_dotnet_api }}document-normalizer-module.html)
- [`NormalizedImageResultItem`]({{ site.ddn_dotnet_api }}normalized-image-result-item.html)
- [`NormalizedImagesResult`]({{ site.ddn_dotnet_api }}normalized-images-result.html)

### Structs

- [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_dotnet_api }}simplified-document-normalizer-settings.html)

### Enums

- [`EnumImageColourMode`]({{ site.dcvb_enumerations }}document-normalizer/image-colour-mode.html?lang=dotnet)

## DynamsoftCodeParser

### Classes

- [`ParsedResultItem`]({{ site.dcp_dotnet_api }}parsed-result-item.html)
- [`ParsedResult`]({{ site.dcp_dotnet_api }}parsed-result.html)

### Enums

- [`EnumMappingStatus`]({{ site.dcvb_enumerations }}code-parser/mapping-status.html?lang=dotnet)
- [`EnumValiadtionStatus`]({{ site.dcvb_enumerations }}code-parser/validation-status.html?lang=dotnet)

## DynamsoftCore

### Classes

- [`CapturedResultItem`]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html)
- [`CoreModule`]({{ site.dcvb_dotnet_api }}core/basic-classes/core-module.html)
- [`FileImageTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/file-image-tag.html)
- [`ImageData`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)
- [`ImageSourceAdapter`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-adapter.html)
- [`IImageSourceErrorListener`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-source-error-listener.html)
- [`ImageTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)
- [`OriginalImageResultItem`]({{ site.dcvb_dotnet_api }}core/basic-classes/original-image-result-item.html)
- [`PDFReadingParameter`]({{ site.dcvb_dotnet_api }}core/basic-classes/pdf-reading-parameter.html)
- [`Point`]({{ site.dcvb_dotnet_api }}core/basic-classes/point.html)
- [`Quadrilateral`]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)
- [`Rect`]({{ site.dcvb_dotnet_api }}core/basic-classes/rect.html)
- [`VideoFrameTag`]({{ site.dcvb_dotnet_api }}core/basic-classes/video-frame-tag.html)

### Structs


### Enums

- [`EnumBufferOverflowProtectionMode`]({{ site.dcvb_enumerations }}core/buffer-overflow-protection-mode.html?lang=dotnet)
- [`EnumCapturedResultItemType`]({{ site.dcvb_enumerations }}core/captured-result-item-type.html?lang=dotnet)
- [`EnumColourChannelUsageType`]({{ site.dcvb_enumerations }}core/colour-channel-usage-type.html?lang=dotnet)
- [`EnumCornerType`]({{ site.dcvb_enumerations }}core/corner-type.html?lang=dotnet)
- [`EnumErrorCode`]({{ site.dcvb_enumerations }}core/error-code.html?lang=dotnet)
- [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_enumerations }}core/grayscale-enhancement-mode.html?lang=dotnet)
- [`EnumGrayscaleTransformationMode`]({{ site.dcvb_enumerations }}core/grayscale-transformation-mode.html?lang=dotnet)
- [`EnumImageCaptureDistanceMode`]({{ site.dcvb_enumerations }}core/image-capture-distance-mode.html?lang=dotnet)
- [`EnumImagePixelFormat`]({{ site.dcvb_enumerations }}core/image-pixel-format.html?lang=dotnet)
- [`EnumImageTagType`]({{ site.dcvb_enumerations }}core/image-tag-type.html?lang=dotnet)
- [`EnumPDFReadingMode`]({{ site.dcvb_enumerations }}core/pdf-reading-mode.html?lang=dotnet)                
- [`EnumRasterDataSource`]({{ site.dcvb_enumerations }}core/raster-data-source.html?lang=dotnet)
- [`EnumRegionObjectElementType`]({{ site.dcvb_enumerations }}core/region-object-element-type.html?lang=dotnet)
- [`EnumSectionType`]({{ site.dcvb_enumerations }}core/section-type.html?lang=dotnet)
- [`EnumTargetType`]({{ site.dcvb_enumerations }}core/target-type.html?lang=dotnet)
- [`EnumVideoFrameQuality`]({{ site.dcvb_enumerations }}core/video-frame-quality.html?lang=dotnet)

## DynamsoftUtility

- [`DirectoryFetcher`]({{ site.dcvb_dotnet_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcvb_dotnet_api }}utility/file-fetcher.html)
- [`ImageManager`]({{ site.dcvb_dotnet_api }}utility/image-manager.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcvb_dotnet_api }}utility/multi-frame-result-cross-filter.html)
- [`ProactiveImageSourceAdapter`]({{ site.dcvb_dotnet_api }}utility/proactive-image-source-adapter.html)
- [`UtilityModule`]({{ site.dcvb_dotnet_api }}utility/utility-module.html)

## DynamsoftLicense

- [`LicenseManager`]({{ site.dcvb_dotnet_api }}license/license-manager.html)
- [`LicenseModule`]({{ site.dcvb_dotnet_api }}license/license-module.html)


## DynamsoftImageProcessing

- [`ImageProcessingModule`]({{ site.dcvb_dotnet_api }}image-processing/image-processing-module.html)


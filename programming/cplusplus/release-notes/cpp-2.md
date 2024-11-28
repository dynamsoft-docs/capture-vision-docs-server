---
layout: default-layout
title: Release Notes v2.x - Dynamsoft Capture Vision Bundle C++ Edition
description: This is the release notes page of Dynamsoft Capture Vision Bundle C++ Edition v2.x.
keywords: release notes, C++
needGenerateH3Content: false
---

# Release Notes for C++ Edition - 2.x

## 2.6.1000 (11/28/2024)

### Highlights

- Enhanced document detection delivers more reliable results, particularly for single-document scenarios. Key improvements include:
  - Strengthened detection algorithms for greater accuracy and robustness.
  - Optimized parameter configurations for better adaptability across diverse scenarios.
  - Refined cross-verification rules to ensure more consistent detection outcomes.

### Changelogs

#### New

- Added a new mode, `CICM_EDGE_ENHANCEMENT`, to the `ColourConversionModes` parameter, designed to enhance edge details when converting a color image to grayscale.
- Introduced the concept of `LogicLines` to enhance the processing and analysis of document structures.
  - Added a new value, `IRUT_LOGIC_LINES`, to the `IntermediateResultUnitType` enumeration.
  - Added a new function `OnLogicLinesReceived` to the class `CIntermediateResultReceiver` which will be called when logic lines have been received.
  - Added a new class, `CLogicLinesUnit`, to represent an intermediate result unit containing logic lines.
- Added the `GetCrossVerificationStatus` function to both the `CDetectedQuadResultItem` and `CNormalizedImageResultItem` classes, along with a new `CrossVerificationStatus` enumeration, to retrieve the cross-verification status of the result.
- Added the `GetParameterTemplateCount` and `GetParameterTemplateName` functions to the `CCaptureVisionRouter` class to improve accessibility and usability of templates.
- Added the `GetFieldRawValue` method to the `CParsedResultItem` class to retrieve the raw value of the field.

#### Fixed

- Fixed a bug in `CTextZone` caused by the absence of a custom copy constructor, which led to improper memory management with the default copy constructor.
- Fixed a bug where the `Default` preset template was not used when the default value was passed for the `templateName` parameter.
- Fixed a potential crash bug during template reading.
- Fixed a bug in DPM mode where the `isMirrored` value in the `CBarcodeResultItem` was not correctly assigned.
- Fixed a bug where DotCode could not be decoded in certain scenarios.
- Small fixes and tweaks.
  
#### Changed

- Updated the parameter configurations for the `DetectDocumentBoundaries_Default` and `DetectAndNormalizeDocument_Default` preset templates to default to single-document mode.
- Changed default value of `ExpectedDocumentsCount` paramter from 0 to 1 to better support single-document mode.
- Changed default value of `CornerAngleRange` paramter from [70, 110] to [60, 120] to support a wider range of document capture angles.
- Modified the return logic for `DetectedQuadResultItem` and `NormalizedImageResultItem` when `ResultCrossVerification` is `enabled`. Previously, only verified results were returned; now, results are returned regardless of verification status, and the results include a `CrossVerificationStatus` to indicate the verification state.
- Removed the `LineExtractMode` parameter and replaced it with `ShortlineDetectionMode` and `LineAssemblyMode` for more flexible and precise configuration.



## 2.4.2000 (10/10/2024)

### Highlights

- Added to-the-latest overlapping feature.
- Added ARM64 and macOS components back to the SDK.
- Improved the error handling logic of methods `Capture`, `StartCapturing` and `InitLicense` to clearly report a licensing issue.

### Changelogs

#### New

- Added new functions [`SetMaxOverlappingFrames`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#setmaxoverlappingframes), [`GetMaxOverlappingFrames`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#getmaxoverlappingframes), [`EnableLatestOverlapping`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#enablelatestoverlapping) and [`IsLatestOverlappingEnabled`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#islatestoverlappingenabled) to the class `CMultiFrameResultCrossFilter`.

- Added new error codes
  - `EC_LICENSE_WARNING`
  - `EC_BARCODE_READER_LICENSE_NOT_FOUND`
  - `EC_LABEL_RECOGNIZER_LICENSE_NOT_FOUND`
  - `EC_DOCUMENT_NORMALIZER_LICENSE_NOT_FOUND`
  - `EC_CODE_PARSER_LICENSE_NOT_FOUND`

#### Fixed

- Fixed a crash bug caused by the usage of RegEx.
- Fixed a bug that could prevent the reading of `GS1_DATABAR_EXPANDED_STACKED` barcodes.
- Small fixes and tweaks.

#### Changed

- Changed the template loading mode. By default, the library loads all template files from the `Templates` folder in the same directory as the library file.
- Changed the enumeration value of `BarcodeFormat::BF_ALL` to 0xFFFFFFFEFFFFFFFF.

### Included Submodules and Their Versions

The following submodules are included in this SDK release along with their respective versions:

- **DynamsoftCaptureVisionRouter** Module: v2.4.20
- **DynamsoftCore** Module: v3.4.20
- **DynamsoftLicense** Module: v3.4.20
- **DynamsoftUtility** Module: v1.4.20
- **DynamsoftImageProcessing** Module: v2.4.20
- **DynamsoftBarcodeReader** Module: v10.4.20
- **DynamsoftLabelRecognizer** Module: v3.4.20
- **DynamsoftDocumentNormalizer** Module: v2.4.20
- **DynamsoftCodeParser** Module: v2.4.20
- **DynamsoftCodeParserDedicator** Module: v1.2.30
- **DynamsoftNeuralNetwork** Module: v1.0.20



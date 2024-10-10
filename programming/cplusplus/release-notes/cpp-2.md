---
layout: default-layout
title: Release Notes v2.x - Dynamsoft Capture Vision Bundle C++ Edition
description: This is the release notes page of Dynamsoft Capture Vision Bundle C++ Edition v2.x.
keywords: release notes, C++
needGenerateH3Content: false
---

# Release Notes for C++ Edition - 2.x

## 2.4.2000 (10/10/2024)

### Highlights

- Added to-the-latest overlapping feature.
- Added ARM64 and MacOS components back to the SDK.
- Improved the error handling logic of methods `Capture`, `StartCapturing` and `InitLicense` to clearly report an licensing issue.

### Changelogs

#### New

- Added a new functions [`SetMaxOverlappingFrames`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#setmaxoverlappingframes), [`GetMaxOverlappingFrames`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#getmaxoverlappingframes), [`EnableLatestOverlapping`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#enablelatestoverlapping) and [`IsLatestOverlappingEnabled`]({{ site.dcvb_cpp_api }}utility/multi-frame-result-cross-filter.html#islatestoverlappingenabled) to the class `CMultiFrameResultCrossFilter`.

- Added new error codes
  - `EC_LICENSE_WARNING`: The license is initialized successfully but detected invalid content in your key.
  - `EC_BARCODE_READER_LICENSE_NOT_FOUND`: [Barcode Reader] No license found.
  - `EC_LABEL_RECOGNIZER_LICENSE_NOT_FOUND`: [Label Recognizer] No license found.
  - `EC_DOCUMENT_NORMALIZER_LICENSE_NOT_FOUND`: [Document Normalizer] No license found.
  - `EC_CODE_PARSER_LICENSE_NOT_FOUND`: [Code Parser] No license found.

#### Fixed

- Fixed a crash bug caused by the usage of RegEx.
- Fixed a bug that might cause `GS1_DATABAR_EXPANDED_STACKED` barcode unread.
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



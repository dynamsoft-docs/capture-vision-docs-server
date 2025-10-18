---
layout: default-layout
title: Release Notes v3.x - Dynamsoft Capture Vision Bundle C++ Edition
description: This is the release notes page of Dynamsoft Capture Vision Bundle C++ Edition v3.x.
keywords: release notes, C++
needGenerateH3Content: false
---

# Release Notes for C++ Edition - 3.x

## 3.2.1000 (10/14/2025)

### 🎉Milestone Release
Version 3.2.1000 introduces a series of AI-driven improvements designed to enhance barcode and MRZ detection accuracy, processing speed, and configuration flexibility.

This release focuses on practical performance gains for production environments across retail, logistics, manufacturing, and identity verification workflows.

### ✨ Key Highlights
#### AI-Powered Barcode Detection and Decoding

- 🧠New Localization Models – Introduces [`OneDLocalization`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) and [`DataMatrixQRCodeLocalization`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) neural network models for improved detection of **blurred / low-resolution 1D codes**, or **partially damaged DataMatrix/QR codes**.
- ⚡Specialized Decoders – Adds [`EAN13Decoder`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) and [`Code128Decoder`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) models optimized for **long-distance** and **motion-blurred** decoding scenarios.
- 🔍Redesigned Deblur Model – The [`OneDDeblur`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) model now provides more effective recovery from **motion and focus blur**.
- 🎯Configurable Model Selection – The new `ModelNameArray` parameter supports flexible model loading and fine-grained control for specific barcode types.

#### Precision and Processing Control

- ⚙️Enhanced Deblur Methods – [`DM_DEEP_ANALYSIS`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#dm_deep_analysis) now includes sub-level control with `OneDGeneral`, `TwoDGeneral`, and `EAN13Enhanced` options.
- 🎯Barcode Count Expectation – The new [`ExpectedBarcodesCount`]({{ site.dcvb_parameters_reference }}barcode-format-specification/expected-barcodes-count.html) parameter enables **format-specific quantity control** and **early termination** in fixed-count workflows.
- 🔍Improved Region Detection – The new [`RPM_GRAY_CONSISTENCY`]({{ site.dcvb_parameters_reference }}image-parameter/region-predetection-modes.html#rpm_gray_consistency) mode provides more precise region extraction based on **grayscale uniformity** and **local consistency** for document and label processing.

#### AI-Powered MRZ Detection

- 🚀Neural MRZ Localization – The new [`MRZLocalization`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/localization-modes.html#modelnamearray) model improves region detection accuracy and delivers up to **42.7%** faster processing for MRZ-based document workflows.
- 🎛️Configurable Localization Control – The new [`LocalizationModes`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/localization-modes.html) parameter allows configuration for text line detection.

#### Smart Document Capture

- 🎥Clarity-Based Frame Selection – Automatically selects the sharpest and highest-quality frame in live capture workflows.
- 🔄Cross-Frame Verification – Updated verification algorithms enhance result reliability.

### Performance Highlights

#### Barcode Workflows

- Up to **26.5%** higher read rates under blur conditions with as much as **44%** faster processing.
- Reliable decoding of DataMatrix and QR codes with missing or damaged finder patterns.
- Extended operational range beyond 75 cm for long-distance barcode scanning.

#### Document Workflows

- Improved performance in live video capture environments.
- Consistent document quality through clarity-based frame evaluation.
- Faster MRZ processing for high-throughput identity verification

### Developer Notes

- Backward Compatibility – Fully compatible with existing integrations; no code-level changes required for upgrade.
- Configuration Flexibility – Expanded parameter set allows comprehensive model configuration for scenario-specific tuning.
- Production Stability – All new models validated in enterprise environments.

### Changed

#### Parameter Defaults

- [`MaxThreadsInOneTask`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/max-threads-in-one-task.html): default changed from 4 → 0 (auto-detection).
- [`IncludeTrailingCheckDigit`]({{ site.dcvb_parameters_reference }}barcode-format-specification/include-trailing-check-digit.html): default changed from 1 → 0. Code128 results will no longer include the trailing check digit by default for improved compliance with standard decoding practices.

### Deprecations

- `DeblurModelNameArray` argument of [`DeblurModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html) → use `ModelNameArray`.
- `AppendModelBuffer` method of CaptureVisionRouter → use [`AppendDLModelBuffer`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-methods.html#appenddlmodelbuffer).

## 3.0.6000 (08/06/2025)

### Changed

- `StartCapturing` now stops immediately and returns a license-related error code if none of the tasks have a valid license, instead of proceeding and returning an empty result.

### Fixed

- Fixed a bug that caused a crash when using a specific type of license.
- Fixed various minor bugs and improved overall stability.

## 3.0.4000 (07/15/2025)

### New

- **Tile-Based TIFF Image Support**: Added support for TIFF images with tile-based storage format.

- **Base64 String Conversion**: Enabled bidirectional conversion between `ImageData` and Base64 strings.

- **Template Version Validation**: Introduced version checking for templates to prevent compatibility issues and mismatches.

### Improved

- **White-on-White Document Recognition**: Optimized accuracy for document detection in scenarios where white paper is placed on a white background.

### Changed

- **License Validation Behavior**: Instead of stopping execution immediately on an invalid license module, the library now continues processing and returns results from modules with valid licenses. An error is still reported to indicate the license issue.

- **PDFR License Control Removal**: Removed the license check for the PDFR module.

### Fixed

- Fixed various minor bugs and improved overall stability.

## 3.0.3000 (05/13/2025)

### New

- Added support for appending pages to PDF files generated by `CImageIO.SaveToFile`. Appending to other PDF files is not supported.
- Added a new function [`Retain`]({{ site.dlr_cpp_api }}raw-text-line.html#retain) to the class [`CRawTextLine`]({{ site.dlr_cpp_api }}raw-text-line.html).

### Fixed

- Resolved a performance issue that could cause unusually high CPU and memory usage in some cases.

### Changed

- Removed the licensing requirement for saving PDFs.


## 3.0.1000 (03/04/2025)

### [Highlights](https://www.dynamsoft.com/release-highlights/?product=dcv3.0)

- Workflow Improvements
  - Restructured the parameter control hierarchy at all levels for finer scope definition and more granular process management, with the stage level newly added.
  - Enabled custom combinations and sequences of sections, increasing flexibility and operational customization under specific conditions.
  - Redesigned document normalization sections to better accommodate diverse document processing operations.
  
- Deep Learning Integration
  - Improved the reading rate of 1D barcode by introducing a new deblurring deep-learning model.
  - Enhanced text recognition capabilities with deep learning-based text-line recognition.

- Algorithm Enhancements
  - Enabled deduplication at the Region of Interest (ROI) level to consolidate results from multiple tasks.
  - Enhanced the text recognition workflow by integrating improved multi-step recognition processes and validation methods.
  - Improved the CODE_128 and DataMatrix DeepAnalysis algorithms for better decoding accuracy and performance.
  - Added support for new barcode types: CODE_32, MATRIX_25, KIX, and TELEPEN.
  - Added GS1 Application Identifiers (AI) support for improved code parsing capabilities.

- Engineering Optimizations
  - Unified template-loading logic to reduce I/O overhead.
  - Added support for capturing data from multi-page files, including PDF and TIFF formats.
  - Implemented conversion functionality between `CImageData` and image files, including both on-disk and in-memory files.

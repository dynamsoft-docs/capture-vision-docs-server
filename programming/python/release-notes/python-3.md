---
layout: default-layout
title: Release Notes v3.x - Dynamsoft Capture Vision Bundle Python Edition
description: This is the release notes page of Dynamsoft Capture Vision Bundle Python Edition v3.x.
keywords: release notes, python
needGenerateH3Content: false
---

# Release Notes for Python Edition - 3.x

## 3.4.1000 (02/05/2026)

### Highlights

#### AI-Powered Barcode Detection and Decoding

- **PDF417 Localization Model** – Introduces the [`PDF417Localization`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) neural network model for improved detection of PDF417 barcodes, especially under challenging conditions.

- **Code39/ITF Decoding Model** – Adds the [`Code39ITFDecoder`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) model for enhanced decoding of Code 39 and ITF barcodes under blurred or low-resolution conditions.

- **Deblur Models for 2D Barcodes** – Adds the [`DataMatrixQRCodeDeblur`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) and [`PDF417Deblur`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) models to provide more effective recovery from motion and focus blur for DataMatrix, QR Code, and PDF417 barcodes.

#### ECI (Extended Channel Interpretation) Support

- **ECI Information Return** – Adds support for retrieving Extended Channel Interpretation (ECI) data from barcodes. The new [`ECISegment`]({{ site.dbr_python_api }}eci-segment.html) class, along with the `get_eci_segments()` method in the [`BarcodeResultItem`]({{ site.dbr_python_api }}barcode-result-item.html#get_eci_segments) and [`DecodedBarcodeElement`]({{ site.dbr_python_api }}decoded-barcode-element.html#get_eci_segments) classes, enables access to character encoding information embedded in barcodes.

- **ECI-Based Text Interpretation** – Adds support for interpreting ECI segments during barcode decoding, improving compatibility with international character sets.

#### Performance Improvements

- **On-Demand Model Loading** – Implements lazy loading for AI models, reducing initialization time by loading models only when first needed.

- **Smart Model Selection** – Models are now loaded based on configured barcode formats, minimizing memory usage by excluding unused models.

- **Improved Confidence Scoring** – Enhances confidence score calculation for results from neural network models, providing more accurate quality indicators.

- **DPM Barcode Optimization** – Improves recognition rate for Direct Part Marking (DPM) barcodes commonly used in industrial and manufacturing environments.

#### Identity Document Processing

- **Enhanced Passport Processing** – Improves document edge detection accuracy for passport documents through optimized processing workflows.

- **Portrait Zone Detection** – The `MRZLocalization` model now supports detecting portrait zone on identity documents, enabling automatic extraction of photo regions.

- **New DynamsoftIdentityUtility Module** – Introduces a dedicated module for identity document processing, including the [`IdentityProcessor`]({{ site.dcvb_python_api }}id-utility/identity-processor.html) class with [`find_portrait_zone()`]({{ site.dcvb_python_api }}id-utility/identity-processor.html#find_portrait_zone) method for precise portrait positioning from passports and ID cards.

### New

- Added support for Python 3.14.

- Added [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcvb_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) parameter for filtering barcodes based on aspect ratio constraints.

- Added [`set_result_cross_verification_criteria()`]({{ site.dcvb_python_api }}utility/multi-frame-result-cross-filter.html#set_result_cross_verification_criteria) and [`get_result_cross_verification_criteria()`]({{ site.dcvb_python_api }}utility/multi-frame-result-cross-filter.html#get_result_cross_verification_criteria) methods to `MultiFrameResultCrossFilter` for configurable multi-frame result verification.

- Added [`AuxiliaryRegionElement`]({{ site.dcvb_python_api }}core/intermediate-results/auxiliary-region-element.html) class for representing additional region information detected during processing (e.g., MRZ (Machine Readable Zone), portrait zones).

- Added `ROET_AUXILIARY_REGION` to [`EnumRegionObjectElementType`]({{ site.dcvb_python_api }}core/enum-region-object-element-type.html) enumeration for the new `AuxiliaryRegionElement` class.

- Added auxiliary region element management methods to `LocalizedTextLinesUnit`: [`get_auxiliary_region_elements_count()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#get_auxiliary_region_elements_count), [`get_auxiliary_region_element()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#get_auxiliary_region_element), [`set_auxiliary_region_element()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#set_auxiliary_region_element), [`add_auxiliary_region_element()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#add_auxiliary_region_element), [`remove_auxiliary_region_element()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#remove_auxiliary_region_element), and [`remove_all_auxiliary_region_elements()`]({{ site.dlr_python_api }}localized-text-lines-unit.html#remove_all_auxiliary_region_elements).

- Added new error code [`EC_PORTRAIT_ZONE_NOT_FOUND`]({{ site.dcvb_python_api }}core/enum-error-code.html) for identity document processing.

### Changed

- `capture_multi_pages` now returns results sorted by page number.

- Barcode text encoding fallback changed from UTF-8 to ISO-8859-1 when no ECI information is present in the barcode.

- Updated default value of `compensation` parameter in [`ImageProcessor.convert_to_binary_local()`]({{ site.dcvb_python_api }}utility/image-processor.html#convert_to_binary_local) from 0 to 10.

- [`convert_to_binary_global()`]({{ site.dcvb_python_api }}utility/image-processor.html#convert_to_binary_global) and [`convert_to_binary_local()`]({{ site.dcvb_python_api }}utility/image-processor.html#convert_to_binary_local) of `ImageProcessor` class now support color, binary and grayscale images as input.

- Parser resource files (.json) have been consolidated into encrypted .data files for improved security and simplified distribution:
  - `AADHAAR.data`, `AAMVA_DL_ID.data`, `GS1_AI.data`, `MRTD.data`, `SOUTH_AFRICA_DL.data`, `VIN.data`

### Improved

- Improved license binding stability on macOS devices.

### Removed

- Removed `DataMatrixModuleIsotropic` parameter – use [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcvb_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) instead.

- Removed `MinRatioOfBarcodeZoneWidthToHeight` parameter – use [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcvb_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) instead.

### Fixed

- Fixed incorrect coordinate in barcode result when using neural network models with a specified region.

- Fixed crash and hang issues that could occur in certain scenarios.

- Fixed various minor bugs and improved overall stability.

## 3.2.5000 (12/16/2025)

This release includes security maintenance updates to ensure continued protection of the product.

### Security Updates

- Updated third-party libraries to incorporate the latest security fixes.

### Bug Fixes

- Fixed memory leak, crash, and hang issues in various scenarios.
- Improved stability in multi-threading operations.

## 3.2.1000 (10/14/2025)

### 🎉Milestone Release
Version 3.2.1000 introduces a series of AI-driven improvements designed to enhance barcode and MRZ detection accuracy, processing speed, and configuration flexibility.

This release focuses on practical performance gains for production environments across retail, logistics, manufacturing, and identity verification workflows.

### ✨ Key Highlights
#### AI-Powered Barcode Detection and Decoding

- New Localization Models – Introduces [`OneDLocalization`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) and [`DataMatrixQRCodeLocalization`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) neural network models for improved detection of **blurred / low-resolution 1D codes**, or **partially damaged DataMatrix/QR codes**.
- Specialized Decoders – Adds [`EAN13Decoder`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) and [`Code128Decoder`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) models optimized for **long-distance** and **motion-blurred** decoding scenarios.
- Redesigned Deblur Model – The [`OneDDeblur`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) model now provides more effective recovery from **motion and focus blur**.
- Configurable Model Selection – The new `ModelNameArray` parameter supports flexible model loading and fine-grained control for specific barcode types.

#### Precision and Processing Control

- Enhanced Deblur Methods – [`DM_DEEP_ANALYSIS`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#dm_deep_analysis) now includes sub-level control with `OneDGeneral`, `TwoDGeneral`, and `EAN13Enhanced` options.
- Barcode Count Expectation – The new [`ExpectedBarcodesCount`]({{ site.dcvb_parameters_reference }}barcode-format-specification/expected-barcodes-count.html) parameter enables **format-specific quantity control** and **early termination** in fixed-count workflows.
- Improved Region Detection – The new [`RPM_GRAY_CONSISTENCY`]({{ site.dcvb_parameters_reference }}image-parameter/region-predetection-modes.html#rpm_gray_consistency) mode provides more precise region extraction based on **grayscale uniformity** and **local consistency** for document and label processing.

#### AI-Powered MRZ Detection

- Neural MRZ Localization – The new [`MRZLocalization`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/localization-modes.html#modelnamearray) model improves region detection accuracy and delivers up to **42.7%** faster processing for MRZ-based document workflows.
- Configurable Localization Control – The new [`LocalizationModes`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/localization-modes.html) parameter allows configuration for text line detection.

#### Smart Document Capture

- Clarity-Based Frame Selection – Automatically selects the sharpest and highest-quality frame in live capture workflows.
- Cross-Frame Verification – Updated verification algorithms enhance result reliability.

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
- `append_model_buffer` method of `CaptureVisionRouter` → use [`append_dl_model_buffer`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-methods.html#appenddlmodelbuffer).

### Fixed

- Fixed an issue where accessing `Quadrilateral.points` directly would return random values instead of the expected coordinate points.

## 3.0.6000 (08/06/2025)

### Changed

- `start_capturing` now stops immediately and returns a license-related error code if none of the tasks have a valid license, instead of proceeding and returning an empty result.

### Fixed

- Fixed a bug that caused a crash when using a specific type of license.
- Fixed various minor bugs and improved overall stability.


## 3.0.4100 (07/16/2025)

### Fixed

- Fixed a bug that caused a crash when calling the `get_processed_document_result` method of `CapturedResult`.


## 3.0.4000 (07/15/2025)

### New

- **Tile-Based TIFF Image Support**: Added support for TIFF images with tile-based storage format.

- **Template Version Validation**: Introduced version checking for templates to prevent compatibility issues and mismatches.

### Improved

- **White-on-White Document Recognition**: Optimized accuracy for document detection in scenarios where white paper is placed on a white background.

### Changed

- **License Validation Behavior**: Instead of stopping execution immediately on an invalid license module, the library now continues processing and returns results from modules with valid licenses. An error is still reported to indicate the license issue.

- **PDFR License Control Removal**: Removed the license check for the PDFR module.

### Fixed

- Fixed an issue where the `get_detected_quad_result_items` method of `ProcessedDocumentResult` returned items of the wrong type.
- Fixed various minor bugs and improved overall stability.

## 3.0.3000 (05/15/2025)

### New

- Added support for appending pages to PDF files generated by `ImageIO.save_to_file`. Appending to other PDF files is not supported.
- Added new property [codewords]({{ site.dbr_python_api }}pdf417-details.html#codewords) to the `PDF417Details` class.

### Fixed

- Resolved a performance issue that could cause unusually high CPU and memory usage in some cases.

### Changed

- Removed the licensing requirement for saving PDFs.


## 3.0.2000 (04/09/2025)

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
  - Implemented conversion functionality between `ImageData` and image files, including both on-disk and in-memory files.

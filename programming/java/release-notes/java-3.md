---
layout: default-layout
title: Release Notes v3.x - Dynamsoft Capture Vision Bundle Java Edition
description: This is the release notes page of Dynamsoft Capture Vision Bundle Java Edition v3.x.
keywords: release notes, java
needGenerateH3Content: false
---

# Release Notes for Java Edition - 3.x

## 3.2.1000 (10/14/2025)

🎉 **Milestone Release** - This version introduces groundbreaking AI-powered enhancements that significantly improve accuracy and performance across all barcode and MRZ processing scenarios.

### ✨ Key Highlights

**AI-Powered Barcode Detection & Decoding**
- 🧠 **First-to-Market AI Localization**: Revolutionary `OneDLocalization` and `DataMatrixQRCodeLocalization` neural network models for superior detection of **blurred/low-resolution 1D codes** and **DataMatrix/QR codes with missing or damaged finder patterns**
- ⚡ **Specialized Decoders**: Cutting-edge `EAN13Decoder` and `Code128Decoder` models deliver unprecedented accuracy for **blurred and long-distance** scenarios
- 🔍 **Enhanced Clarity Processing**: Completely redesigned `OneDDeblur` model with superior **motion blur and focus blur** recovery algorithms
- 🎯 **Flexible Model Configuration**: Advanced `ModelNameArray` parameter enables on-demand model loading and precise selection for specific barcode scenarios

**Precision Control**
- ⚙️ **Granular Deblur Methods**: Fine-tuned `DM_DEEP_ANALYSIS` with specialized method control - `OneDGeneral`, `TwoDGeneral`, and `EAN13Enhanced` for targeted optimization
- 🎯 **Smart Barcode Counting**: New `ExpectedBarcodesCount` parameter enables **format-specific quantity control** and **early termination optimization** for known-quantity scenarios
- 🔍 **Advanced Region Detection**: New `RPM_GRAY_CONSISTENCY` mode enables precise region detection based on **grayscale uniformity** and **local consistency** for document and label processing


**Enhanced Text Processing**
- 🚀 **High-Speed and Precise MRZ Region Detection**: Revolutionary neural network `MRZLocalization` model delivers **42.7% faster processing** with enhanced region detection accuracy for passport and ID workflows
- 🎛️ **Advanced Localization**: New `LocalizationModes` parameter provides unprecedented control over text line detection algorithms


**Smart Document Capture**
- 🎥 **Clarity-Based Frame Selection**: Intelligent frame selection automatically chooses the sharpest, highest-quality document images
- 🔄 **Enhanced Cross-Frame Verification**: Advanced cross-frame verification algorithms significantly improve result reliability and accuracy


### 💡 What This Means for You

**For Challenging Barcode Scenarios**
- **Blurred conditions**: 26.5% better read rates with 44% faster processing - ideal for handheld scanning and moving objects
- **Extended distance capability**: Breakthrough support for reading distances beyond 75cm - revolutionizing warehouse automation and high-shelf scanning
- **Damaged 2D codes**: Enhanced detection of DataMatrix and QR codes with missing or damaged finder patterns - perfect for manufacturing and logistics applications

**For Document Processing Applications**
- **Real-time video streams**: Optimized performance maintains smooth user experience in live capture scenarios
- **Document quality assessment**: Intelligent clarity-based frame selection ensures highest quality document captures

**For Enterprise Integration**
- **Retail environments**: Enhanced performance for blurred handheld scanning and long-distance shelf reading
- **Logistics & shipping**: Improved recognition for package tracking with better blur and long-distance scanning capabilities
- **Manufacturing QC**: Improved 2D code reading on printed/etched parts with wear damage  
- **Security applications**: Faster MRZ processing for high-throughput identity verification

**For Developers**
- **Backward Compatible**: Seamless upgrade with existing code and easy migration path
- **Flexible Configuration**: Extensive parameter customization for specific use cases and comprehensive model configuration options
- **Enterprise Ready**: Battle-tested stability for production environments

### Changed

- Updated the default value of parameter [`MaxThreadsInOneTask`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/max-threads-in-one-task.html) from 4 to 0 (auto-detection).
  - Updated the default value of parameter [`IncludeTrailingCheckDigit`]({{ site.dcvb_parameters_reference }}barcode-format-specification/include-trailing-check-digit.html) from 1 to 0. This means Code128 barcode results will no longer include the trailing check digit in the decoded bytes by default, improving compatibility with industry standards.
- Deprecated argument `DeblurModelNameArray` of parameter [`DeblurModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html), use `ModelNameArray` instead.
- Deprecated method `appendModelBuffer` of class [`CaptureVisionRouter`]({{ site.dcvb_java_api }}capture-vision-router/capture-vision-router.html), use [`appendDLModelBuffer`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-methods.html#appenddlmodelbuffer) instead.

## 3.0.6100 (08/19/2025)

### Fixed

- Fixed an issue where using a callback function could cause the program to crash.

## 3.0.6000 (08/06/2025)

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

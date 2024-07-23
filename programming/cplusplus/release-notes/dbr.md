---
layout: default-layout
title: DBR Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftBarcodeReader module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, barcode reader, CPP, DBR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftBarcodeReader Module

## 10.4.10 (07/23/2024)

### Improved

- Improved the read rate and speed of the following barcode format:
  - EAN-13
  - DotCode

### New

- Added support for decoding add-on codes (also known as Extension Codes) for UPC-A, UPC-E, EAN-8 and EAN-13 codes.
- Added new properties to the [`CQRCodeDetails`]({{ site.dbr_cpp_api }}qr-code-details.html) class
  - [`dataMaskPattern`]({{ site.dbr_cpp_api }}qr-code-details.html#dataMaskPattern)
  - [`codewords`]({{ site.dbr_cpp_api }}qr-code-details.html#codewords)
  - [`codewordsCount`]({{ site.dbr_cpp_api }}qr-code-details.html#codewordsCount)
- Added a new function [`AddItem`]({{ site.dbr_cpp_api }}decoded-barcodes-result.html#additem) to the class [`CDecodedBarcodesResult`]({{ site.dbr_cpp_api }}decoded-barcodes-result.html).
- Added a new function [`SetLocation`]({{ site.dbr_cpp_api }}barcode-result-item.html#setlocation) to the class [`CBarcodeResultItem`]({{ site.dbr_cpp_api }}barcode-result-item.html).

## 10.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftBarcodeReader` library.

### Fixed

- Fixed a misreading bug of the PDF417 barcodes on the South Carolina driver's license.
- Internal changes to prevent crash bugs in barcode decoding.

## 10.2.0 (01/16/2024)

### New

- Added new methods to the `CCandidateBarcodeZonesUnit` class to add, remove or set the candidate barcode zones. `CCandidateBarcodeZone` class is added to store the information of a single candidate barcode zone.
- Added new methods to the `CLocalizedBarcodesUnit` class to add, remove or set the localized barcode elements.
- Added a new method `SetImageData` to the `CScaledUpBarcodeImageUnit` class.
- Added new methods to the `CDeformationResistedBarcodeImageUnit` class to add, remove or set the deformation-resisted barcode. `CDeformationResistedBarcode` class is added to store the deformation-resisted barcode information.
- Added a new method SetLocation to `CComplementedBarcodeImageUnit` class.
- Added new methods to the `CDecodedBarcodesUnit` class to set or remove the decoded barcode elements.
- Added the following methods to the `CDecodedBarcodesResult` class:
  - `operator[]`
  - `Retain`
  - `Release`.
- Added the following methods to the `CBarcodeReaderModule` class to create the corresponding elements.
  - `CreateDecodedBarcodeElement`
  - `CreateLocalizedBarcodeElement`
- Added the following methods to the `CDecodeBarcodeElement` class to modify the basic information of the barcode:
  - `SetFormat`
  - `SetText`
  - `SetBytes`
  - `SetConfidence`
- Added a new method `SetPossibleFormats` to the `CLocalizedBarcodeElement`.
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The destructor functions of the following classes are changed to protected:
  - `CCandidateBarcodeZonesUnit`
  - `CLocalizedBarcodesUnit`
  - `CScaledUpBarcodeImageUnit`
  - `CDeformationResistedBarcodeImageUnit`
  - `CComplementedBarcodeImageUnit`
  - `CDecodedBarcodesUnit`
  - `CDecodedBarcodeElement`
  - `CLocalizedBarcodeElement`
  - `CDecodedBarcodesResult`
  - `CBarcodeResultItem`
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 10.0.20 (10/26/2023)

### New

- Added a new parameter `scaleDownThreshold` to the struct `SimplifiedBarcodeReaderSettings`.

### Fixed

- Small fixes and tweaks.

### Break Changes

- Removed `BF_PATCH_CODE` from the combined value of `BF_DEFAULT` as decoding Patch Code is not supported by default.

## 10.0.10 (08/08/2023)

### Break Changes

- Renamed the method `GetCount` of `CDecodedBarcodesResult` class to `GetItemsCount`.
- Renamed the method `GetSourceImageHashId` of `CDecodedBarcodesResult` class to `GetOriginalImageHashId`.
- Renamed the method `GetSourceImageTag` of `CDecodedBarcodesResult` class to `GetOriginalImageTag`.

## 10.0.0 (07/04/2023)

The first version of `DynamsoftBarcodeReader (DBR)` CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.

---
layout: default-layout
title: License Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftLicense module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, license, CPP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLicense Module

## 3.2.30 (07/23/2024)

### New

- Added a new charge way, `TimeSliceCount`.

### Changed

- Changed the maximum length of the `name` parameter to 255 for the [`SetDeviceFriendlyName`]({{ site.dcv_cpp_api }}license/license-manager.html#setdevicefriendlyname) method. If the length exceeds 255, it will be truncated.

## 3.2.20 (04/07/2024)

### Fixed

- Small fixes and tweaks.

## 3.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftLicense` library.
- Improved the usage count logic of the concurrent license mode.
- Improved the experience of local cache usage when failing to connect the license server. The renewal of the local cache is optimized as well.

### Fixed

- Fixed a bug where the capture might be blocked due to the network latency.
- Fixed a bug where the `DetectAndNormalizeDocument` task might be approved without a valid license.
- Fixed the bugs of usage count.
  - Count twice for a single PDF417 barcode when a code parser task is implemented on the result.
  - The barcode decoding result might not be uploaded timely.
  - The usage count of text line recognition might be double counted when the intermediate results are output.
  - The document boundary detection result might be miscounted.
  - Patchcode might be counted even if there is no Patchcode license item.

## 3.2.0 (01/16/2024)

### New

- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 3.0.40 (02/01/2024)

### Fixed

- Small fixes and tweaks.

## 3.0.30 (12/07/2023)

### Fixed

- Fixed a bug that might cause the app frozen.

## 3.0.20 (10/26/2023)

### Changed

- The `initLicense` method will return error when you input contains correct and incorrect key at the same time.

## 3.0.10 (08/08/2023)

### Fixed

- Fixed a bug where the local license is not successfully updated in some cases.

## 3.0.0 (07/04/2023)

The first version of `DynamsoftLicense`.

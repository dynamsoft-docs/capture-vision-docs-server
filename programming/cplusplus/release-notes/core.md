---
layout: default-layout
title: Core Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of Dynamsoft Capture Vision CPP Edition.
keywords: release notes, core, CPP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - Core Module

## 3.2.1 (02/29/2024)

### Improved

- Security update for `DynamsoftCore` library.

### New

- Added new error codes:
  - `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE`
  - `EC_LICENSE_CACHE_USED`
- Added a virtual destructor to the interface [`CImageSourceErrorListener`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-error-listener.html) to prevent memory leaks.

### Fixed

- Fixed a crash bug of the Replace method of the [`IntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) class. The method will return the error code `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE` when the result type is mismatched.

## 3.2.0 (01/16/2024)

### New

- Added the following methods to the [`CObservationParameters`]({{ site.dcv_cpp_api }}core/intermediate-results/observation-parameters.html) class to specify the `input only` result unit.
  - `SetResultUnitTypesOnlyForInput`
  - `GetResultUnitTypesOnlyForInput`
  - `IsResultUnitTypeOnlyForInput`
- Added the following methods to the `CRegionObjectElement` class to support the intermediate result modification.
  - `SetLocation`
  - `Clone`
  - `Retain`
  - `Release`
- Added a new method `Replace` to the `CIntermediateResultUnit` class to support the replacement of intermediate result units.
- Added `SetImageData` methods to the following classes:
  - `CColourImageUnit`
  - `CScaledDownColourImageUnit`
  - `CGrayscaleImageUnit`
  - `CTransformedGrayscaleImageUnit`
  - `CEnhancedGrayscaleImageUnit`
  - `CBinaryImageUnit`
  - `CTextureRemovedGrayscaleImageUnit`
  - `CTextureRemovedBinaryImageUnit`
  - `CTextRemovedBinaryImageUnit`
- Added new methods to the `CPredetectedRegionsUnit` class to add, remove or set the predetected regions.
- Added new methods to the `CLineSegmentsUnit` class to add, remove or set the line segments.
- Added new methods to the `CTextZonesUnit` class to add, remove or set the text zones. Added a new class CTextZone to store the information of a single text zone.
- Added a new method `SetContours` to the `CContourUnit` class.
- Added new methods to the `CTextureDetectionResultUnit` class to set the X & Y spacing.
- Added a new intermediate result unit, `CShortLinesUnit`, to output the detected short lines. The corresponding enumeration member IRUT_SHORT_LINES is added to the `IntermediateResultUnitType`.
- Added the following methods to the `CCapturedResultItem` class
  - `GetTargetROIDefName`
  - `GetTaskName`
  - `Retain`
  - `Release`
- Added the following new error codes
  - `EC_IMAGE_SIZE_NOT_MATCH`
  - `EC_IMAGE_PIXEL_FORMAT_NOT_MATCH`
  - `EC_SECTION_LEVEL_RESULT_IRREPLACEABLE`
  - `EC_AXIS_DEFINITION_INCORRECT`
  - `EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT`
  - `EC_TEXT_LINE_GROUP_REGEX_CONFLICT`
- Added the following methods to the `CCapturedResult` class.
  - A new override constructor.
  - `Retain`
  - `Release`
- Added a new class `CAbstractIntermediateResultReceiver`. It is the super class of the `CIntermediateResultReceiver`.
- The following classes are moved to `CaptureVisionRouter` module:
  - `CIntermediateResultReceiver`
  - `CapturedResultReceiver`
  - `CapturedResultFilter`
  - `CintermediateResultManager`
- Updated `CImageData` class
  - Change the return value of `GetBytesLength` from int to unsigned long long.
  - Added a new constructor.
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the `ImagePixelFormat`.
- Added return value for the `Retain` method of the `CIntermediateResultUnit` class. The method will return the pointer of the current `CIntermediateResultUnit`.
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The destructor functions of the following classes are changed to protected
  - `CCapturedResult`
  - `CCapturedResultItem`
  - `CRegionObjectElement` and its subclasses
  - `CIntermediateResultUnit` and its subclasses
- Refactored the `CContour` class. Please view API reference - `CContour` class for more information.
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

### Fixed

- Fixed a crash bug that might happen when triggering the `SetNextImageToReturn` method of the `ImageSourceAdapter` class.

## 3.0.30 (02/01/2024)

### New

- Added a new virtual function to obtain resources based on the specified template.

## 3.0.20 (10/26/2023)

### New

- Added `ImageSourceErrorListener` to receive the errors from an image source.
- Added method `setErrorListener` to class `ImageSourceAdapter` to add the `ImageSourceErrorListener`.
- Added the following error codes:
  - `EC_FILE_ALREADY_EXISTS`
  - `EC_CREATE_FILE_FAILED`
  - `EC_IMGAE_DATA_INVALID`

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the timing of `onOriginalImageResultReceived` so that it is triggered immediately after receiving the image.

## 3.0.10 (08/08/2023)

### New

- Added a new class `CVector4` in the core module.
- Added new methods `SetTransformMatrix` and `GetTransformMatrix` to the class `CIntermediateResultUnit`. Enumeration `TransformMatrixType` is also added to support users specifying the type of the target matrix.
- Added method `GetContours` to the class `CContourUnit` to get all the `CContour` objects contained in the unit and their hierarchies.
- Added enumeration `RasterDataSource` to specify the raster data source when reading PDF files. The previous enumeration `TargetType` is removed. The attribute `TargetType` type of Class `CPDFReadingParameter` is replaced by `RasterDataSource`.

### Fixed

- Fixed crash bugs that happen in rare cases.
- Other small fixes and tweaks.

### Changed

- Renamed methods `GetCount` of `CCapturedResult` class to `GetItemsCount`.
- Renamed method `GetSourceImageHashId` to `GetOriginalImageHashId`. This change applies to the following classes:
  - `CIntermediateResultUnit`
  - `CCapturedResult`
- Renamed method `GetSourceImageTag` to `GetOriginalImageTag`. This change applies to the following classes:
  - `CIntermediateResultUnit`
  - `CCapturedResult`
- Renamed method `OnRawImageResultReceived` to `OnOriginalImageResultReceived`. This change applies to the following classes:
  - `CapturedResultReceiver`
  - `CapturedResultFilter`
- Renamed a method of `CIntermediateResultManager` from `GetRawImage` to `GetOriginalImage`.
- Renamed the class `CRawImageResultItem` to `COriginalImageResultItem`.
- Renamed an enumeration member of `CapturedResultItemType` from `CRIT_RAW_IMAGE` to `CRIT_ORIGINAL_IMAGE`.
- Renamed an enumeration member of `BufferOverflowProtectionMode` from `BOPM_APPEND` to `BOPM_UPDATE`.
- Renamed the enumeration `TargetType` to `RasterDataSource`.

### Removed

- Removed methods `SetLocalToSourceImageTransformMatrix` and `GetLocalToSourceImageTransformMatrix` from class `CIntermediateResultUnit`.
- Removed methods `SetRotationTransformMatrix` and `GetRotationTransformMatrix` from class `CIntermediateResultUnit`.
- Removed methods `GetCount` and `GetContour` from class `CContourUnit`. Use the method `GetContours` instead.

## 3.0.0 (07/04/2023)

The first version of `DynamsoftCore` CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
